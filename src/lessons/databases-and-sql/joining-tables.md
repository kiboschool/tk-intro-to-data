## Combining multiple tables
In our bookstore example, imagine we need to generate reports showing not just what books were sold, but also who bought them and when. We cannot achieve this only by focusing on just one _Books_ table. We'll need to pull data from different tables to answer such complex questions.

<!-- Joining tables thus enables the integration of related data stored in different tables, providing a more holistic view of the bookstore's operations -->


<aside>

**_Definition..._** 

**_JOIN_** merges records from two tables by comparing the values of columns in one table with the values of columns in the other table.
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe width="100%" height="415" src="https://www.youtube.com/embed/G3lJAxg1cdfgy8?si=8jtdMo8m3hhdgOBmkb5" title="Linking your CSS" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

Joins are crucial in relational databases because they allow for the combination of data from two or more tables based on a related column between them. This is essential for creating comprehensive datasets that can answer complex queries by pulling together relevant information from different tables.

### Types of Joins
Let's consider two simplified tables from our bookstore database to illustrate how different types of SQL joins work:

![book-order-tables](./databases-and-sql/tables.png)

<!-- `Books`

| BookID | Title            |
|--------|------------------|
| 1      | The Great Escape |
| 2      | Enchanted Night  |
| 3      | Lost Horizons    |

`Orders`

| OrderID | BookID | Quantity |
|---------|--------|----------|
| 1       | 1      | 2        |
| 2       | 2      | 1        |
| 4       | 4      | 1        |  <!-- Note: BookID 4 does not match any BookID in the Books table -->

<!-- #### INNER JOIN
Combines rows from both tables that have matching values in the joined columns.

**SQL Query**:
```sql
SELECT Orders.OrderID, Books.Title, Orders.Quantity
FROM Orders
INNER JOIN Books ON Orders.BookID = Books.BookID;
```

**Result**:

| OrderID | Title            | Quantity |
|---------|------------------|----------|
| 1       | The Great Escape | 2        |
| 2       | Enchanted Night  | 1        |

#### LEFT OUTER JOIN
Returns all rows from the left table (Orders), and the matched rows from the right table (Books). If there's no match, the result is NULL on the right side.

**SQL Query**:
```sql
SELECT Orders.OrderID, Books.Title, Orders.Quantity
FROM Orders
LEFT OUTER JOIN Books ON Orders.BookID = Books.BookID;
```

**Result**:

| OrderID | Title            | Quantity |
|---------|------------------|----------|
| 1       | The Great Escape | 2        |
| 2       | Enchanted Night  | 1        |
| 4       | NULL             | 1        | <!-- Note: No matching BookID in Books table -->

<!-- #### RIGHT OUTER JOIN
Returns all rows from the right table (Books), and the matched rows from the left table (Orders). If there's no match, the result is NULL on the left side.

**SQL Query**:
*This example shows what would happen in a database that supports RIGHT OUTER JOINs, assuming an additional unmatched book in the `Books` table.*

**Result**:

| OrderID | Title            | Quantity |
|---------|------------------|----------|
| 1       | The Great Escape | 2        |
| 2       | Enchanted Night  | 1        |
| NULL    | Lost Horizons    | NULL     | Note: No matching OrderID in Orders table -->

<!-- #### FULL OUTER JOIN
Combines the results of both LEFT OUTER JOIN and RIGHT OUTER JOIN. All rows from both tables are returned, with NULL values in places where there is no match.

**SQL Query**:
*Assuming support for FULL OUTER JOIN, this query combines all previous examples.*

**Result**:

| OrderID | Title            | Quantity |
|---------|------------------|----------|
| 1       | The Great Escape | 2        |
| 2       | Enchanted Night  | 1        |
| 4       | NULL             | 1        | <!-- No matching BookID in Books table -->
<!-- | NULL    | Lost Horizons    | NULL     | <!-- No matching OrderID in Orders table 

### Practical Example: African Presidential Election (Hypothetical)

Assuming we're analyzing a different scenario unrelated to the bookstore, such as an African presidential election, with `Candidates` and `Votes` tables. The previous section discussed how to join these tables. Here, the focus was on demonstrating joins with the bookstore example, emphasizing the direct impact of different joins on the query results by illustrating how matched and unmatched records are handled.  -->