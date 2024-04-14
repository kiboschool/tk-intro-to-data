# Exploring Looker Studio

## Data Connectors
Imagine you have different storage places for your data, like a big library with lots of books. Now, think of data connectors as special tools that help you easily find and bring those books from different shelves in the library to your desk, so you can read and analyze them. 

In Looker Studio, these connectors work like magical bridges between your data sources (like databases, spreadsheets, or cloud services) and Looker, making it simple for you to access and explore your data without having to do any heavy lifting. 


<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://edpuzzle.com/embed/assignments/661c4972b10f47a72e265bfd/watch" title="Data Visualization" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>


Now that you have an understanding of what connectors are and different ones available in Looker studio, we'll now focus on using Google Sheet connector in this lesson. 

## Add google sheet to Looker
Adding Google Sheets to Looker involves setting up a connection between your Google Sheets and Looker, allowing you to seamlessly import and analyze your spreadsheet data within the Looker studio. To connect your dataset in google sheet, follow the steps in the video below.

<br>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/-GEcAv8kLj4?si=o46583ST3HLlxJQp" title="Data Visualization" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

In summary, connecting your data in google sheet to looker studio is just a few clicks 🎯 away by following the steps below.

- Create Data Source
    - On the Looker Studio homepage, click on the `+ Create` button and select Data Source from the dropdown menu.
    - You'll be taken to the Connect to Data page, where you can see a variety of `data connectors`.

- Select Google Sheets Connector:
    - Find and click on the `Google Sheets` connector. You might need to scroll through the list or use the search bar.
    - Grant the necessary permissions if prompted.

- Choose Your Spreadsheet:
    - Select the spreadsheet that contains your bookstore data. Then, select the specific worksheet.
    - Click on the Connect button in the top right corner to establish the connection between your Google Sheet and Looker Studio.

Once you have your data successfully loaded your data into _Looker_, we can now explore different things we can do with the data. Let's start with cleaning our data.
<!-- Simple Practice: Connect a Google Sheet that contains sample book sales data from your bookstore example to Looker Studio and visualize the number of books sold. -->

### Data Cleaning in Looker

Just like sorting through your clothes to remove any wrinkles or stains, data cleaning in Looker involves identifying and fixing any errors, inconsistencies, or missing values in your data. This ensures that when you analyze your data, you can trust the results and make informed decisions based on accurate information.

Conseuently, data cleaning in Looker is essential because it helps make our data more reliable and easier to work with, ultimately leading to better insights and smarter decision-making. It's like giving your data a makeover, so it's polished and presentable for analysis 🥰.

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://edpuzzle.com/embed/assignments/661c53f140c3b7b8c284b2f0/watch" title="Data Visualization" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

To summarise data cleaning functionalities in Looker studio, remember to note the following points:
- **Identifying missing values**
    - Look for `no data`, `zeros`, or `unknowns` in reports as they can skew analysis.
- **Handling missing values**: 
    - It's crucial to decide whether to remove or keep them, considering the proportion relative to the dataset.
    - Utilize filters or controls to remove null values, but be cautious as it may affect other data.
    - Options like _showing no data_ or _replacing with zeros_ are also methods of dealing with missing values, ensuring clarity in visualization.
- **Data types**
    - Incorrect data types, such as treating numeric values as text, can lead to wrong conclusions; ensure proper data type assignment for accurate analysis.

<!-- ### 2. Removing duplicates

Just like removing duplicates entries in your phone contacts, removing duplicates using Looker ensures that each record is unique by streamlining and simplifying the dataset to eliminate redundant information.

<br>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/-GEcAvj8kLj4?si=o46583ST3HLlxJQp" title="Data Visualization" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>
 -->


<aside>

**_Remember...!_**

- You can clean your dataset using google sheet before importing into Looker
- If cleaning your data on Looker, make sure Looker provides all the cleaning functionalities you need.
</aside>


### 👩🏾‍🎨 **`Practice: Data Connectors`**

Imagine you are a data analyst at a retail company, and your team is interested in analyzing data from various sources using Looker Studio. Your task is to connect to different data sources.

**Instructions**:
1. Connect to a CSV file containing sales data using the `File Upload` connector in Looker Studio.
2. Connect to a Google Sheets document containing inventory data using the `Google Sheets` connector.
3. Connect to a SQL database containing customer data using the `SQL` connector.
4. Once connected to each data source, verify the connection status and **ensure that data is successfully imported into Looker Studio**.

**Submission**:
- Take a snippet of your Looker studio inface after importing data from all the sources
- Upload the screenshot/snippet to **[this padlett](https://padlet.com/curriculumpad/showcase-your-looker-studio-insights-fedtq1ttpesamw0y)**.


<aside>

**➡️ In the next section...**
- We'll look at how to create dashboards.
</aside>
