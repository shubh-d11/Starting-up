## Answers for SQL assignment 1

### 1. Add a column somewhere to create a link between the payments and orders.

#### Some obnservations:
* No. of orders >  No. of payments which means their could be multiple orders for a payment or vice versa.
* Payment per order can be extracted from order details by grouping on order numbers and selecting the sum(priceForEach*quantity)
* After adding such a column to the orders table and making the joins with customers and payments, 23 payments do not find a match.
* No. of orders which are not shipped = 23(just a coincidence)
* After grouping on such tables, it is seen that 3 Resolved orders have been payed off, which means 23 was just a coincidence.

#### Conclusion:
We can not be sure of a one to one relationship between the payments and orders, so we can add a new table orderPaymentDetail which can have the foreign key's orderNumber and checkNumber to map a many to many relationship. Also , we cannot map orders and payments for the past data because of the lack of information.
We create the table like this:

```
create table orderpaymentdetails (
     customerNumber int NOT NULL,
     refId int PRIMARY KEY,
     orderNumber int NOT NULL,
     checkNumber varchar(50) NOT NULL,
     constraint fk_1 foreign key(orderNumber) references orders(orderNumber),
     constraint fk_2 foreign key(customerNumber, checkNumber) references payments(customerNumber, checkNumber)
     );
```

### 2. Reading done

### 3. Transactions

#### We start off by creating a new customer in the following way:

```

start transaction;

select @customerNumber:=MAX(customerNumber)+1
       from customers;

INSERT INTO customers(customerNumber,
     customerName,
     contactLastName,
     contactFirstname,
     phone,
     addressLine1,
     addressLine2,
     city,
     state,
     postalCode,
     country,
     salesRepEmployeeNumber,
     creditLimit)
VALUES(@customerNumber,
     'Shubh Gupta',
     'Gupta',
     'Shubh',
     '7318019018',
     'asdadad',
     'asddadad',
     'faridabad',
     'haryana',
     '121003',
     'India',
     1002,
     100);

INSERT INTO orders(orderNumber,
                   orderDate,
                   requiredDate,
                   shippedDate,
                   status,
                   customerNumber)
VALUES(@orderNumber,
       '2005-05-31',
       '2005-06-10',
       '2005-06-11',
       'In Process',
        @customerNumebr);
        
INSERT INTO orderdetails(orderNumber,
                         productCode,
                         quantityOrdered,
                         priceEach,
                         orderLineNumber)
VALUES(@orderNumber,'S18_1749', 30, '136', 1),
      (@orderNumber,'S18_2248', 50, '55.09', 2);

insert into payments(
     customerNumber,
     checkNumber,
     paymentDate,
     amount)
     VALUES(
     @customerNumber,
     'HQ336336',
     '2020-06-06',
     25000);        //only used a random amount, it should've been chosen according to the quantity and priceEach in orderdetails.


```
