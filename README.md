 

#1

use billing_simple;

select * from billing where payer_email= 'vasya@mail.com'

#2

use billing_simple;

insert into billing (payer_email, recipient_email, sum, currency, billing_date, comment) values('pasha@mail.com', 'katya@mail.com', 300, 'EUR', '2016-02-14', 'Valentines day present)')

#3

use billing_simple;

UPDATE billing SET payer_email= 'alex@mail.com' where 'payer_email'= 'igor@mail.com';

#4

use billing_simple;

delete from billing where recipient_email= NULL or recipient_email= '';

#5

USE project_simple;

SELECT count(project_name) FROM project

#6

USE store_simple;

SELECT category, count(category) FROM store GROUP BY category

#7

USE store_simple;

SELECT category, count(category), Max(price) FROM store

GROUP BY price

ORDER by price desc

LIMIT 5;

#8

USE project_simple;

SELECT count(project_name), sum(budget), avg(datediff(project_start, project_finish)) FROM project




Степик
#1

use billing_simple;

select * from billing where payer_email= 'vasya@mail.com'

#2

use billing_simple;

insert into billing (payer_email, recipient_email, sum, currency, billing_date, comment) values('pasha@mail.com', 'katya@mail.com', 300, 'EUR', '2016-02-14', 'Valentines day present)')

#3

use billing_simple;

UPDATE billing SET payer_email= 'alex@mail.com' where 'payer_email'= 'igor@mail.com';

#4

use billing_simple;

delete from billing where recipient_email= NULL or recipient_email= '';

#5

USE project_simple;

SELECT count(project_name) FROM project

#6

USE store_simple;

SELECT category, count(category) FROM store GROUP BY category

#7

USE store_simple;

SELECT category, count(category), Max(price) FROM store

GROUP BY price

ORDER by price desc

LIMIT 5;

#8

USE project_simple;

SELECT count(project_name), sum(budget), avg(datediff(project_start, project_finish)) FROM project

INSERT INTO book (title, author, price, amount)
VALUES (N'Мастер и Маргарита', N'Булгаков М.А.', 670.99, 3)

INSERT INTO book (title, author, price, amount)
VALUES ('Белая гвардия', 'Булгаков М.А.', 540.50, 5),
('Идиот', 'Достоевский Ф.М.', 460.00, 10),
('Братья Карамазовы', 'Достоевский Ф.М.', 799.01, 2);
