# Top_SQL_Queries
Top more than 30 queries of SQL

1.	Write a SQL statement that displays all the information about all salespeople.

  	SELECT * FROM salesman;
    ![P1](https://github.com/user-attachments/assets/6cfdca1d-7c16-4c72-9929-abd5bed7099b)

2.	Write a SQL statement to display a string "This is SQL Exercise, Practice and   Solution".

  	SELECT 'This is SQL Exercise, Practice and Solution';
    ![P2](https://github.com/user-attachments/assets/58b81c7f-2cc8-4c27-9861-cc6a55b090d0)

3.	Write a SQL query to display three numbers in three columns.

  	SELECT 5,10,15;
  	![P3](https://github.com/user-attachments/assets/e700fe54-9d83-49ef-b332-ccc2179fc1f1)


4.	Write a SQL query to display the sum of two numbers 10 and 15 from the RDBMS server.

  	SELECT 10+15;
  	![P4](https://github.com/user-attachments/assets/8c5a698c-c978-4f91-9609-9133a03b5176)
  
5.	Write an SQL query to display the result of an arithmetic expression. 

  	SELECT 10+15-5*2;
  	![P5](https://github.com/user-attachments/assets/6a744d8e-22fd-4ba7-ac08-7838f4e084bb)

6. Write a SQL statement to display specific columns such as names and commissions for all salespeople.

    SELECT name, commission FROM salesman;
   ![P6](https://github.com/user-attachments/assets/028dc585-7bb6-49e7-8227-b4f628a8f503)
    
7.	Write a query to display the columns in a specific order, such as order date, salesman ID, order number, and purchase amount for all orders.  

   	SELECT ord_date, salesman_id, ord_no, purch_amt FROM orders;
   	![P7](https://github.com/user-attachments/assets/ab94b6f3-7c41-4d85-9312-69b24d1611b9)

8. From the following table, write a SQL query to identify the unique salespeople ID. Return salesman_id.

    SELECT DISTINCT salesman_id FROM orders;
    ![P8](https://github.com/user-attachments/assets/bfae5d55-1641-4beb-8b3d-a6e4b602bdd2)

9. From the following table, write a SQL query to locate salespeople who live in the city of 'Paris'. Return salesperson's name, city.

    SELECT name, city FROM salesman WHERE city='Paris';
    ![P9](https://github.com/user-attachments/assets/7e49313b-a1f7-4e92-aa5b-122f3cd6364e)

10. From the following table, write a SQL query to find customers whose grade is 200. Return customer_id, cust_name, city, grade, salesman_id.

    SELECT * FROM customer WHERE grade=200;
    ![P10](https://github.com/user-attachments/assets/df80c83d-0489-41fa-ade3-ec2dcf8c5546)

11. From the following table, write a SQL query to find orders that are delivered by a salesperson with ID. 5001. Return ord_no, ord_date, purch_amt.

    SELECT ord_no, ord_date FROM orders WHERE salesman_id=5001;
    ![P11](https://github.com/user-attachments/assets/61876ac4-6d05-4878-9222-92f179bbe5e4)

12. From the following table, write a SQL query to find the Nobel Prize winner(s) for the year 1970. Return year, subject and winner.

    SELECT YEAR, SUBJECT, WINNER FROM nobel_win WHERE YEAR=1970;
    ![P12](https://github.com/user-attachments/assets/376b13ae-5186-434d-88d9-807509f623bf)

20. From the following table, write a SQL query to find the Nobel Prize winner in ‘Literature’ for 1971. Return winner.

    SELECT WINNER FROM nobel_win WHERE SUBJECT='Literature' AND YEAR=1971;
    ![P13](https://github.com/user-attachments/assets/41c13101-4d2d-47a3-b75a-24da573cc52d)

21. From the following table, write a SQL query to locate the Nobel Prize winner ‘Dennis Gabor'. Return year, subject.

    SELECT YEAR,SUBJECT FROM nobel_win WHERE WINNER='Dennis Gabor';
    ![P14](https://github.com/user-attachments/assets/4796e653-ce7b-40e4-a080-e0f2e49b451c)

22. From the following table, write a SQL query to find the Nobel Prize winners in the field of ‘Physics’ since 1950. Return winner.

    SELECT WINNER FROM nobel_win WHERE SUBJECT='Physics' and YEAR>1950;
    ![P15](https://github.com/user-attachments/assets/3bf33b63-df98-480c-89f3-46e7885d6251)

23. From the following table, write a SQL query to find the Nobel Prize winners in ‘Chemistry’ between the years 1965 and 1975. Begin and end values are included. Return year, subject, winner, and country.

    SELECT YEAR, SUBJECT, WINNER, COUNTRY FROM nobel_win WHERE SUBJECT="Chemistry" AND YEAR BETWEEN 1965 and 1975;
    ![P16](https://github.com/user-attachments/assets/7a46ba32-44f2-4dd3-b421-12d96c7fb8a2)

24. Write a SQL query to display all details of the Prime Ministerial winners after 1972 of Menachem Begin and Yitzhak Rabin.

    SELECT * FROM nobel_win WHERE YEAR>1972 AND WINNER IN ('Menachem Begin', 'Yitzhak Rabin');
    ![P17](https://github.com/user-attachments/assets/ecff2a8a-291b-410b-aefc-abffd4fee9b2)

25. From the following table, write a SQL query to retrieve the details of the winners whose first names match with the string ‘Louis’. Return year, subject, winner, country, and category.

    SELECT YEAR, SUBJECT, WINNER, COUNTRY, CATEGORY FROM nobel_win WHERE WINNER LIKE 'Louis%';
    ![P18](https://github.com/user-attachments/assets/3f3062cb-509f-4987-9731-e1e36c29de6a)

26. From the following table, write a SQL query that combines the winners in Physics, 1970 and in Economics, 1971. Return year, subject, winner, country, and category.

    SELECT * FROM nobel_win WHERE (SUBJECT='Physics' AND YEAR=1970)
    UNION
    (select * FROM nobel_win WHERE (SUBJECT='Economics' AND YEAR=1971));
    ![P19](https://github.com/user-attachments/assets/e7cc3845-699b-4450-a899-2e6d41320964)

28. From the following table, write a SQL query to find the Nobel Prize winners in 1970 excluding the subjects of Physiology and Economics. Return year, subject, winner, country, and category.

    SELECT * FROM nobel_win WHERE SUBJECT in ('Physiology', 'Economics') AND YEAR=1970
    ![P20](https://github.com/user-attachments/assets/b2c4365e-175e-4a55-8814-a57dfe19d4a3)

29. From the following table, write a SQL query to combine the winners in 'Physiology' before 1971 and winners in 'Peace' on or after 1974. Return year, subject, winner, country, and category.

    SELECT * FROM nobel_win WHERE (SUBJECT='Physiology' AND YEAR<=1971)
    UNION
    (SELECT * FROM nobel_win WHERE (SUBJECT='Peace' AND YEAR>=1974));
    ![P21](https://github.com/user-attachments/assets/3cacfdd0-996e-4c1d-ae64-77ab061a8897)

30. From the following table, write a SQL query to find the details of the Nobel Prize winner 'Johannes Georg Bednorz'. Return year, subject, winner, country, and category.

    SELECT * FROM nobel_win WHERE YEAR>1972 and WINNER="Johannes Georg Bednorz"
    ![P22](https://github.com/user-attachments/assets/7c0a0055-d1aa-4a27-896c-fee93c5fd133)

31. From the following table, write a SQL query to find Nobel Prize winners for the subject that does not begin with the letter 'P'. Return year, subject, winner, country, and category. Order the result by year, descending and winner in ascending.

    SELECT * FROM nobel_win WHERE SUBJECT NOT like 'P%' ORDER BY YEAR DESC, WINNER;
    ![P23](https://github.com/user-attachments/assets/3a7a5bab-5b0a-4716-a715-4bb3ce86929a)

32. From the following table, write a SQL query to find the details of 1970 Nobel Prize winners. Order the results by subject, ascending except for 'Chemistry' and ‘Economics’ which will come at the end of the result set. Return year, subject, winner, country, and category.

    SELECT YEAR, SUBJECT, WINNER, CATEGORY FROM nobel_win WHERE YEAR=1970 ORDER BY CASE WHEN SUBJECT IN('Chemistry', 'Economics') THEN 1 ELSE 0 END, SUBJECT;
    ![P24](https://github.com/user-attachments/assets/ac058d56-0563-4887-96f4-e971df8991d2)

33. From the following table, write a SQL query to select a range of products whose price is in the range Rs.200 to Rs.600. Begin and end values are included. Return pro_id, pro_name, pro_price, and pro_com.

    SELECT * FROM item_mast WHERE PROPRICE BETWEEN 200 AND 600;
    ![p25](https://github.com/user-attachments/assets/1630969a-2546-40d1-8e22-3dfe164b699b)

34. From the following table, write a SQL query to calculate the average price for a manufacturer code of 16. Return avg.

    SELECT AVG(PROPRICE) FROM item_mast WHERE PROCOM=16
    ![P26](https://github.com/user-attachments/assets/ff726248-cd42-45dc-99d3-17286d1a5f77)

36. From the following table, write a SQL query to display the pro_name as 'Item Name' and pro_priceas 'Price in Rs.'

    SELECT PRONAME AS 'ITEM NAEM', PROPRICE AS 'Price' FROM item_mast
    ![P27](https://github.com/user-attachments/assets/e62eaa3f-e2f3-415c-a786-0393282ef074)

37. From the following table, write a SQL query to find the items whose prices are higher than or equal to $250. Order the result by product price in descending, then product name in ascending. Return pro_name and pro_price.

    SELECT PRONAME, PROPRICE FROM item_mast WHERE PROPRICE>=250 ORDER BY PROPRICE DESC, PRONAME
    ![P28](https://github.com/user-attachments/assets/f71a3686-76ae-455b-8f20-df9a9dac2ae9)

38. From the following table, write a SQL query to calculate average price of the items for each company. Return average price and company code.

    SELECT AVG(PROPRICE) AS AVG, PROCOM FROM item_mast GROUP BY PROCOM
    ![P29](https://github.com/user-attachments/assets/a9ca5622-979f-4243-90eb-ba9294f3e6a6)

39. From the following table, write a SQL query to find the cheapest item(s). Return pro_name and, pro_price.

    SELECT PRONAME, PROPRICE FROM item_mast WHERE PROPRICE=(SELECT min(PROPRICE) FROM item_mast)
    ![P30](https://github.com/user-attachments/assets/f2d79b6f-b98c-4918-b36a-74e04c0d6314)

40. From the following table, write a SQL query to find the unique last name of all employees. Return emp_lname.

    SELECT DISTINCT EMPLNAME FROM emp_detai
    ![P31](https://github.com/user-attachments/assets/c1b54873-94ed-41c1-8d01-6e4e6684b463)

41. From the following table, write a SQL query to find the details of employees whose last name is 'Snares'. Return emp_idno, emp_fname, emp_lname, and emp_dept.

    SELECT * FROM emp_detail WHERE EMPLNAME="Snares"
    ![P32](https://github.com/user-attachments/assets/12195412-ebf8-4d17-9b92-d45bf8edb124)

42. From the following table, write a SQL query to retrieve the details of the employees who work in the department 57. Return emp_idno, emp_fname, emp_lname and emp_dept.

    SELECT * FROM emp_detail WHERE Emp_Dept=57
    ![P33](https://github.com/user-attachments/assets/aa53a95f-1aa7-47d5-978c-3a3060596451)




