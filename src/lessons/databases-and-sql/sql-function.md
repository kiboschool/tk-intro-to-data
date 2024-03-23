# SQL Function

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
> **'`*`'** means EVERYTHING or ALL

**Output**:
```
TotalBooks | TotalGenres
-----------|------------
3          | 3
------------------------
```

#### SUM()
In our bookstore example, we can use this function to calculate the total quantity of books sold, alongside the total number of orders. For example,

```sql
SELECT SUM(Quantity) AS TotalQuantitySold, 
COUNT(OrderID) AS TotalOrders FROM Orders;
```
**Output**:
```
TotalQuantitySold | TotalOrders
------------------|------------
4                 | 3
-------------------------------
```

### AVG()
In our bookstore example, we can use this function to determine the average price of books, alongside the count (i.e., total number) of books. For example,

```sql
SELECT AVG(Price) AS AveragePrice, 
COUNT(BookID) AS TotalBooks FROM Books;
```
**Output**:
```
AveragePrice | TotalBooks
-------------|-----------
17.33        | 3
-------------------------
```

### MAX() and MIN()
In our bookstore example, we can use this function to find the highest and lowest price of books. For example,

```sql
SELECT MAX(Price) AS HighestPrice, 
MIN(Price) AS LowestPrice FROM Books;
```

**Output**:
```
HighestPrice | LowestPrice
-------------|------------
20           | 10
--------------------------
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
**Output**:
```
UppercaseTitle  | LowercaseAuthor
----------------|----------------
THE GREAT ESCAPE| john doe
ENCHANTED NIGHT | jane smith
LOST HORIZONS   | emily brontë
---------------------------------
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
These functions extracts the year, month, and day from publication dates. Below is an example of how to use these functions in our bookstore example

```sql
SELECT Title, YEAR(PublishDate) AS PublicationYear, 
MONTH(PublishDate) AS PublicationMonth, 
DAY(PublishDate) AS PublicationDay FROM Books;
```
**Output**:
```
Title            | PublicationYear | PublicationMonth | PublicationDay
-----------------|-----------------|------------------|----------------
The Great Escape | 2018            | 5                | 15
Enchanted Night  | 2020            | 7                | 22
Lost Horizons    | 2017            | 3                | 8
-----------------------------------------------------------------------
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
**Output** (sample prices are assumed):
```
Title            | RoundedPrice | CeilPrice | FloorPrice
-----------------|--------------|-----------|-----------
The Great Escape | 15           | 15        | 14
Enchanted Night  | 20           | 20        | 19
Lost Horizons    | 12           | 12        | 11
--------------------------------------------------------
```


<!-- ## Subqueries
Imagine you're on a treasure hunt, and you have a map that leads you to a spot where you find another map to the actual treasure. Subqueries work like that second map. They help break down complex questions into smaller, manageable parts. 

So, if you're trying to figure out something tricky with your data, like finding only the most popular books sold last month, subqueries help by first identifying what counts as "most popular" before getting you the detailed list. It's like solving a puzzle piece by piece instead of trying to see the whole picture all at once.

<aside>

**_Definition..._** 

**_Subqueries_** are basically a query inside another query. They allow for more complex operations and can be used in _INSERT, UPDATE,  DELETE, SELECT, FROM_, and _WHERE_ clauses among others.
</aside> --> 

<aside>

**_Chapter summary...✍🏾_**


</aside>

### 👩🏾‍🎨 **`Practice: SQL Functions`**


<aside>

**➡️ In the next section...**
- We'll look at some practice exercises on what we have covered so far this week.
</aside>
