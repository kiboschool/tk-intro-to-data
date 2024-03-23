## SQL Function & Subqueries

### SQL Functions
SQL functions are built-in operations in SQL that allow for processing and manipulation of data directly within your queries. They can perform calculations, convert data types, and many more, by simplifying complex tasks into manageable commands.

In this lesson, we'll be looking at 2 categories of SQL functions:
- Built-in functions
- User defined function 

### Built-in Functions
These are predefined operations used to perform specific tasks that involves data manipulation, transformation, or analysis within your queries. They are integral to SQL and are supported across various database management systems, except for some little variations. Based on what each function is doing, they are generally categorized as follows:

#### Aggregate Functions
Aggregate functions are used for calculations on a set of values and return a single value, making them essential for statistical analysis over rows of a table.

<!-- COUNT(): Counts the number of rows in a dataset.
SUM(): Calculates the total sum of a numeric column.
AVG(): Determines the average value of a numeric column.
MAX(): Finds the maximum value in a column.
MIN(): Finds the minimum value in a column.

### 5. SQL Functions

#### Definition and Usage
SQL functions are built-in operations in SQL that allow for processing and manipulation of data directly within your queries. They can perform calculations, convert data types, and more, simplifying complex tasks into manageable commands.

#### Use Cases with Outputs

1. **Aggregate Functions**

**Code Snippet**:
```sql
SELECT COUNT(*) AS TotalBooks
FROM Books;
```
**Output**:
```
TotalBooks
----------
3
```
This query calculates the total number of books in the `Books` table, indicating the size of the bookstore's inventory.

2. **String Functions**

**Code Snippet**:
```sql
SELECT UPPER(Title) AS BookTitle
FROM Books;
```
**Output**:
```
BookTitle
-----------------
THE GREAT ESCAPE
ENCHANTED NIGHT
LOST HORIZONS
```
All book titles are converted to uppercase, ensuring uniform text format for titles in reports or listings.

3. **Date and Time Functions**

**Code Snippet**:
```sql
SELECT Title, YEAR(PublishDate) AS YearPublished
FROM Books;
```
**Output** (Assuming sample publish dates for illustration):
```
Title            | YearPublished
-----------------|---------------
The Great Escape | 2018
Enchanted Night  | 2020
Lost Horizons    | 2017
```
This retrieves the publication year for each book, useful for organizing or analyzing books based on their release year.

4. **Conditional Functions**

**Code Snippet**:
```sql
SELECT Title, 
       CASE 
           WHEN Price < 10 THEN 'Budget'
           WHEN Price BETWEEN 10 AND 20 THEN 'Premium'
           ELSE 'Luxury'
       END AS PriceCategory
FROM Books;
```
**Output** (Assuming sample prices for illustration):
```
Title            | PriceCategory
-----------------|--------------
The Great Escape | Premium
Enchanted Night  | Budget
Lost Horizons    | Luxury
```
Books are categorized by price, providing a quick reference to their pricing tier, which can help in marketing or sales analysis.

SQL functions significantly enhance the capability to process and analyze data within SQL queries, enabling more complex data manipulation and analysis directly in the database with minimal effort. These examples showcase how SQL functions can be utilized to generate meaningful insights and data transformations effortlessly.

1. **Aggregate Functions**

**Code Snippet**:
```sql
SELECT COUNT(*) AS TotalBooks
FROM Books;
```
**Output**:
```
TotalBooks
----------
3
```
This query calculates the total number of books in the `Books` table, indicating the size of the bookstore's inventory.

2. **String Functions**

**Code Snippet**:
```sql
SELECT UPPER(Title) AS BookTitle
FROM Books;
```
**Output**:
```
BookTitle
-----------------
THE GREAT ESCAPE
ENCHANTED NIGHT
LOST HORIZONS
```
All book titles are converted to uppercase, ensuring uniform text format for titles in reports or listings.

3. **Date and Time Functions**

**Code Snippet**:
```sql
SELECT Title, YEAR(PublishDate) AS YearPublished
FROM Books;
```
**Output** (Assuming sample publish dates for illustration):
```
Title            | YearPublished
-----------------|---------------
The Great Escape | 2018
Enchanted Night  | 2020
Lost Horizons    | 2017
```
This retrieves the publication year for each book, useful for organizing or analyzing books based on their release year.

4. **Conditional Functions**

**Code Snippet**:
```sql
SELECT Title, 
       CASE 
           WHEN Price < 10 THEN 'Budget'
           WHEN Price BETWEEN 10 AND 20 THEN 'Premium'
           ELSE 'Luxury'
       END AS PriceCategory
FROM Books;
```
**Output** (Assuming sample prices for illustration):
```
Title            | PriceCategory
-----------------|--------------
The Great Escape | Premium
Enchanted Night  | Budget
Lost Horizons    | Luxury
```
Books are categorized by price, providing a quick reference to their pricing tier, which can help in marketing or sales analysis.

SQL functions significantly enhance the capability to process and analyze data within SQL queries, enabling more complex data manipulation and analysis directly in the database with minimal effort. These examples showcase how SQL functions can be utilized to generate meaningful insights and data transformations effortlessly.







## Subqueries
Imagine you're on a treasure hunt, and you have a map that leads you to a spot where you find another map to the actual treasure. Subqueries work like that second map. They help break down complex questions into smaller, manageable parts. 

So, if you're trying to figure out something tricky with your data, like finding only the most popular books sold last month, subqueries help by first identifying what counts as "most popular" before getting you the detailed list. It's like solving a puzzle piece by piece instead of trying to see the whole picture all at once.

<aside>

**_Definition..._** 

**_Subqueries_** are basically a query inside another query. They allow for more complex operations and can be used in _INSERT, UPDATE,  DELETE, SELECT, FROM_, and _WHERE_ clauses among others.
</aside> -->