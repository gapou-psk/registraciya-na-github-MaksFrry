USE store;
SELECT category.name AS category_name , good.name AS good_name FROM category_has_good as chg
INNER JOIN good
ON good.id = chg.good_id
INNER JOIN category
ON category.id = chg.category_id
ORDER BY good_name

SELECT * FROM billing WHERE payer_email='vasya@mail.com'

USE billing;
INSERT INTO billing(payer_email) VALUES ('pasha@mail.com');
INSERT INTO billing(recipient_email) VALUES ('katya@mail.com');
INSERT INTO billing(sum) VALUES ('300.00');
INSERT INTO billing(currency) VALUES ('EUR');
INSERT INTO billing(billing_date) VALUES ('14.02.2016');
INSERT INTO billing(comment) VALUES ('Valentines day present');
SELECT * FROM billing WHERE SUM=300;

USE billing;
UPDATE billing
SET 
payer_email='igor@mail.com'
WHERE payer_email='alex@mail.com';

USE billing;
DELETE FROM billing
WHERE payer_email= '' or recipient_email='';

USE project_simple;
SELECT count(project_name) FROM project

USE store_simple;
SELECT category, count(category) FROM store GROUP BY category

USE store_simple;
SELECT category, count(category), Max(price) FROM store
GROUP BY price
ORDER by price desc
LIMIT 5;

USE project_simple;
SELECT count(project_name), sum(budget), avg(datediff(project_start, project_finish)) FROM project

