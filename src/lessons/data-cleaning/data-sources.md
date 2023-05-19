# Data Sources and Collection
As a data scientist, you'll work with different types of data from different sources. It is important to understand not just these data sources but also how to collect the data therein. To achieve this, we'll be looking at 4 different data sources; _databases, APIs, web scraping_, and _data streams_.

![data-sources-image](./data-cleaning/data-sources.jpeg)

### _What are data sources?_

<aside>

**_Definition_**

Data sources are locations where historic, live, static or streaming data originates from. These sources allow data to be stored, managed, and accessed while holding either raw and/or refined data.

</aside>

## Databases
A database is an organized collection of structured information, or data, typically stored electronically in a computer system. Databases can store information about people, products, orders, transactions, or anything else using one or multiple tables. Each table is made up of rows and columns in a relational database, and records within each table is identified using a **primary key**. For example, the image below shows 4 tables; _Customer, Order, Product_, and _Invoice_. Each of this table has a primary key (Customer_id, Order_id, Product_id, Invoice_id) to  uniquely identifies each record.

![database-with-tables](./data-cleaning/databse-tables.png)

As shown below, multiple tables are linked together for easy access and retrieval. All this is usually controlled by a database management system (DBMS), where data can then be easily accessed, managed, modified, updated, and organized using _Structured Query Language (SQL)_.  An example SQL query to retrieve customers' record from a database is given below.

> **Note**: the table name and the retrieved data are imaginary

<code>

| Query                             | Description                                                    |
| --------------------------------- | -------------------------------------------------------------- |
| **SELECT * FROM CUSTOMER** | Retrieve all records or data from the customer table |

</code>

After running the query above, an example data that could be retrieved is given in the table below. It is evident that are modelled into rows and columns where each row represent a customer information.

|   | Customer ID | Name      | Email                                                 | Unit Price | Total Price | Status          | Order Date                |  |
| - | ----------- | --------- | ----------------------------------------------------- | ---------- | ----------- | --------------- | ------------------------- |  |
| 1 | JD342       | John Doe  | john.doe@example.com   | 50         | 100         | Paid            | 2022-12-19 |
| 2 | BL876       | Bruce Lee | bruce.lee@example.com | 100        | 100         | Awiting payment | 2022-12-12 |


### Application Programming Interface (API)

<aside>

**Definition...**

API is a method of allowing two or more applications to talk to each other using an agreed protocol (or rule). This means one application would be able to access certain data or information from the other.

</aside>

When we pull or check our phone for weather data, a request will be sent to your weather app which resides on a server that stores all the weather information. Behind the scene, an API is used to send a request to the weather app server and gotten a response which is the weather data you see on your phone. As depicted below, an API serves as an intermediary that allows a data scientist to access data from databases or other locations.

![api-request](./data-cleaning/api-request.png)

Now, let us look at different format of data we can get while using an API. As a data scientist, the most common data format are `csv, json`, and `xml`. Below is an example of how each data of this data format looks like.

Sample json data...
<code>

```
    {

        "crust"": "original",

        "toppings"": ["cheese","pepperoni"", "garlic""],

        "status"": "cooking"

    }
```

</code>

<!-- Sample csv data...

<code>
    column 1 name,column 2 name, column 3 name<br>
    first row data 1,first row data 2,first row data 3<br>
    second row data 1,second row data 2,second row data 3`

</code> -->