## SQL Functions
SQL functions are built-in operations in SQL that allow for processing and manipulation of data directly within your queries. With these, we can perform calculations, convert data types, and many more, by simplifying complex tasks into manageable commands.

In SQL, there are 2 categories of SQL functions. 
- _Built-in functions_.
- _User-defined functions_.

However, we'll only focus on _built-in_ functions for this lesson.

### Built-in Functions
These are predefined operations used to perform specific tasks that involves data manipulation, transformation, or analysis within your queries. They are integral to SQL and are supported across various database management systems, except for some little variations. Based on what each function is doing, they are generally categorized as follows:

### Aggregate Functions
Aggregate functions are used for calculations on a set of values where they return a single value, making them essential for statistical analysis over rows of a table. To understand this, let's look at different aggregate functions and how to use them in the context of our bookstore example.

- `COUNT()`: Counts the number of rows in a dataset.
- `SUM()`: Calculates the total sum of a numeric column.
- `AVG()`: Determines the average value of a numeric column.
- `MAX()`: Finds the maximum value in a column.
- `MIN()`: Finds the minimum value in a column.

#### COUNT() 
In our bookstore example, we can use this function to count the total number of books and total genres. For example,

```sql
SELECT COUNT(*) AS TotalBooks, 
COUNT(DISTINCT Genre) AS TotalGenres FROM Books;
```

**<a href="https://onecompiler.com/mysql/429ktre2n" target="_blank"> Try IT! </a>**


**Output**:
```
----------------------------
| TotalBooks | TotalGenres |
----------------------------
|          6 |           5 |
----------------------------
```

#### SUM()
In our bookstore example, we can use this function to calculate the total quantity of books sold, alongside the total number of orders. For example,

```sql
SELECT SUM(Quantity) AS TotalQuantitySold, 
COUNT(OrderID) AS TotalOrders FROM Orders;
```

**<a href="https://onecompiler.com/mysql/429kv3qe3" target="_blank"> Try IT! </a>**

```
-----------------------------------
| TotalQuantitySold | TotalOrders |
-----------------------------------
|                 4 |           3 |
-----------------------------------
```

### AVG()
In our bookstore example, we can use this function to determine the average price of books, alongside the count (i.e., total number) of books. For example,

```sql
SELECT AVG(Price) AS AveragePrice, 
COUNT(BookID) AS TotalBooks FROM Books;
```

**<a href="https://onecompiler.com/mysql/429mtmmtd" target="_blank"> Try IT! </a>**


**Output**:
```
+--------------+------------+
| AveragePrice | TotalBooks |
+--------------+------------+
|      12.5000 |          6 |
+--------------+------------+
```

### MAX() and MIN()
In our bookstore example, we can use this function to find the highest and lowest price of books. For example,

```sql
SELECT MAX(Price) AS HighestPrice, 
MIN(Price) AS LowestPrice FROM Books;
```

**<a href="https://onecompiler.com/mysql/429mu26hp" target="_blank"> Try IT! </a>**

**Output**:
```
+--------------+-------------+
| HighestPrice | LowestPrice |
+--------------+-------------+
|        15.99 |        9.99 |
+--------------+-------------+
```

### String Functions
String functions are used to manipulate, examine, or handle text data (strings). Below are the different types of functions in this category. To understand this, let's look at different string functions and how to use them in the context of our bookstore example.
- `UPPER()`: Converts a string to uppercase.
- `LOWER()`: Converts a string to lowercase.
- `LENGTH()`: Returns the length of a string.
- `TRIM()`: Removes leading and trailing spaces from a string.
- `CONCAT()`: Joins two or more strings together.


### UPPER() and LOWER()
In our bookstore example, this function will converts book titles to uppercase and author names to lowercase. For example,

```sql
SELECT UPPER(Title) AS UppercaseTitle, 
LOWER(Author) AS LowercaseAuthor FROM Books;
```

**<a href="https://onecompiler.com/mysql/429muv4y5" target="_blank"> Try IT! </a>**

**Output**:
```
+----------------------+-----------------+
| UppercaseTitle       | LowercaseAuthor |
+----------------------+-----------------+
| THE ENCHANTED FOREST | jane doe        |
| THE FOREST           | tal kil         |
| THE LOST KINGDOM     | john smith      |
| MYSTERY MANSION      | emily brown     |
| THE SECRET GARDEN    | sarah johnson   |
| THE HIDDEN TREASURE  | david lee       |
+----------------------+-----------------+
```

### LENGTH() and TRIM()
For our bookstore example, this function will get the length of book titles and trims authors' names. For example,

```sql
SELECT Title, LENGTH(Title) AS TitleLength, 
TRIM(Author) AS TrimmedAuthor FROM Books;
```
**Output**:
```
Title            | TitleLength | TrimmedAuthor
-----------------|-------------|---------------
The Great Escape | 15          | John Doe
Enchanted Night  | 14          | Jane Smith
Lost Horizons    | 13          | Emily Brontë
-----------------------------------------------
```

### Date and Time Functions
Date and time functions allow you to manipulate and extract portions of dates and times. Below are the different types of functions in this category. To understand this, let's look at different date and time functions and how to use them in the context of our bookstore example.
- `NOW()`: Returns the current date and time.
- `CURDATE()`: Returns the current date.
- `DATE_ADD()`: Adds a specified time interval to a date.
- `DATEDIFF()`: Calculates the difference between two dates.
- `YEAR()`, `MONTH()`, `DAY()`: Extract the year, month, and day from a date, respectively.


### YEAR(), MONTH(), and DAY()
These functions extracts the year, month, and day from a date. Below is an example of how to use these functions in our bookstore example

```sql
SELECT Title, PublishDate AS OriginalDate,
YEAR(PublishDate) AS PublicationYear, 
MONTH(PublishDate) AS PublicationMonth, 
DAY(PublishDate) AS PublicationDay FROM Books;
```

**<a href="https://onecompiler.com/mysql/429mv3tt4" target="_blank"> Try IT! </a>**

**Output**:
```
+----------------------+--------------+-----------------+------------------+----------------+
| Title                | OriginalDate | PublicationYear | PublicationMonth | PublicationDay |
+----------------------+--------------+-----------------+------------------+----------------+
| The Enchanted Forest | 2023-03-15   |            2023 |                3 |             15 |
| The Forest           | 2023-03-15   |            2023 |                3 |             15 |
| The Lost Kingdom     | 2023-04-01   |            2023 |                4 |              1 |
| Mystery Mansion      | 2023-02-20   |            2023 |                2 |             20 |
| The Secret Garden    | 2023-05-10   |            2023 |                5 |             10 |
| The Hidden Treasure  | 2023-03-25   |            2023 |                3 |             25 |
+----------------------+--------------+-----------------+------------------+----------------+
```

## Numeric/Mathematical Functions
These functions perform mathematical calculations on numeric data. Below are the different types of functions in this category. To understand this, let's look at different numeric/mathematical functions and how to use them in the context of our bookstore example.
- `ROUND()`: Rounds a number to a specified number of decimal places.
- `ABS()`: Returns the absolute value of a number.
- `CEIL()` or `CEILING()`: Rounds a number up to the nearest integer.
- `FLOOR()`: Rounds a number down to the nearest integer.
- `RAND()`: Generates a random number.

### ROUND(), CEIL(), and FLOOR()
Below is an example showing how to use these functions in our bookstore example.

```sql
SELECT Title, ROUND(Price, 0) AS RoundedPrice, CEIL(Price) AS CeilPrice, 
FLOOR(Price) AS FloorPrice FROM Books;
```

**<a href="https://onecompiler.com/mysql/429mvdcnx" target="_blank"> Try IT! </a>**

**Output** (sample prices are assumed):
```
+----------------------+--------------+-----------+------------+
| Title                | RoundedPrice | CeilPrice | FloorPrice |
+----------------------+--------------+-----------+------------+
| The Enchanted Forest |           16 |        16 |         15 |
| The Forest           |           10 |        10 |          9 |
| The Lost Kingdom     |           13 |        13 |         12 |
| Mystery Mansion      |           11 |        11 |         10 |
| The Secret Garden    |           10 |        10 |          9 |
| The Hidden Treasure  |           15 |        15 |         14 |
+----------------------+--------------+-----------+------------+
```


<!-- ## Subqueries
Imagine you're on a treasure hunt, and you have a map that leads you to a spot where you find another map to the actual treasure. Subqueries work like that second map. They help break down complex questions into smaller, manageable parts. 

So, if you're trying to figure out something tricky with your data, like finding only the most popular books sold last month, subqueries help by first identifying what counts as "most popular" before getting you the detailed list. It's like solving a puzzle piece by piece instead of trying to see the whole picture all at once.

<aside>

**_Definition..._** 

**_Subqueries_** are basically a query inside another query. They allow for more complex operations and can be used in _INSERT, UPDATE,  DELETE, SELECT, FROM_, and _WHERE_ clauses among others.
</aside> --> 



### 👩🏾‍🎨 **`Practice: SQL Functions`**

Consider the following student table:

**Students**

```
+-----------+-----------+-----+-------+
| StudentID | Name      | Age | Grade |
|-----------|-----------|-----|-------|
| 1         | John      | 18  | 85    |
| 2         | Alice     | 17  | 92    |
| 3         | Michael   | 19  | 78    |
| 4         | Emily     | 16  | 88    |
| 5         | Chris     | 18  | 95    |
+-----------+-----------+-----+-------+
```

Using this `Students` table, write SQL queries to perform the following tasks:

1. Calculate the average age of all students.
2. Count the number of students who are older than 17 years
3. Find the maximum grade achieved by any student.
4. Calculate the sum of all grades.
5. Retrieve the name and grade of the top-performing student.

#### Submission
- Submit your SQL queries using **[this repl](https://replit.com/team/tk11-ids/Practice-SQL-Functions)**

<br>

<aside>

**➡️ In the next section...**
- We'll look at some practice exercises on what we have covered so far this week.
</aside>
