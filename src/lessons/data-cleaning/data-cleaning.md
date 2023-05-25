# 🔢 Data cleaning techniques
As a data scientist, we'll be working with lots of messy (or smelling 😖) data everyday. However, it is critical to ensure the accuracy, reliability, and integrity of the data by carefully _cleaning_ the data (without water 😁). In this lesson, we'll be looking at different data cleaning techniques needed to get the data ready for further analysis. First, we'll start by exploring techniques needed to handle `missing data`. Next, we'll see how to handle `duplicate` data. Lastly, we'll learn how to handle incosistent data formats like `dates`.

<img src="./data-cleaning/data-cleaning-techniques.jpeg" height="300px" width="100%">

<aside>

**_What is data cleaning?_**

_Data cleaning,_ also known as _data cleansing_ or _data preprocessing_. It involves identifying and correcting errors, inconsistencies, and inaccuracies in the dataset to ensure its quality and reliability for further analysis. 

</aside>

Data cleaning aims to improve the integrity, completeness, and consistency of the data. When cleaning a data, our goal will be to produce a clean and reliable dataset that is ready for further analysis. By investing time and effort into data cleaning, we can improve the accuracy and credibility of our analysis results, leading to more robust and reliable insights. To understand this more, we'll be looking at the following

- Handling missing data
- Removing duplicate data values 
- Handling inconsistencies with Dates
<!--
- Dealing with outliers -->

### 1. Handling missing data
Missing data is one of the most frequently occuring problems you can face as a data scientist. Watch the next video to have an idea of how important it is to understand this problem, and possible causes.

> 📺 How important are missing data? 👨🏾‍💻 

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/BqtTcOtkp6Y" title="Web Scrapping Intro" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

As a data scientist, there are many ways of dealing with missing values in a data. For this lesson, we'll be looking at 3 different techniques of handling missing data -  _dropping, filling with constant, filling with statistics, forward or backward filling_, and _interpolation_. 

> **NOTE**: In a Pandas dataframe, missing values are represented with `NaN`.

#### Dropping missing values
One straightforward approach is to remove rows or columns with missing values using the `dropna()` function. By specifying the appropriate axis parameter, you can drop either rows `(axis=0)` or columns `(axis=1)` that contain any missing values. However, this approach should be used with **caution** as it may result in a **loss of valuable data**.

```
    # Drop column with any missing values
    df.dropna(axis=1, inplace=True)

    # Drop rows with any missing values
    df.dropna(axis=0, inplace=True)

```

![drop-column](./data-cleaning/drop_column.png)

![drop-row](./data-cleaning/drop_row.png)

#### Filling with constant
You can also fill missing values with a constant value using the `fillna()` function. This can be done for specific columns or the entire DataFrame. For example, filling missing values with zero:

    # Fill missing values in a specific column
    df['Serious cases'].fillna(0, inplace=True)

    # Fill missing values in the entire DataFrame
    df.fillna(0, inplace=True)

![filling-with-constant](./data-cleaning/filling-with-constant.png)
![filling-dataframe-with-constant](./data-cleaning/fillin-dataframe-with-constant.png)

#### Filling missing values with statistics
Another approach is to fill missing values with summary statistics, such as _mean, median_, or _mode_. Pandas provides convenient functions like `mean()`, `median()`, and `mode()` to compute these statistics. For example, filling missing values with the mean of column `Serious cases`:

    # Fill missing values in a specific column with the mean
    df['Serious cases'].fillna(df['Serious cases'].mean(), inplace=True)

![filling-with-mean](./data-cleaning/filling-with-mean.png)

#### Filling with interpolation
Pandas supports different interpolation methods to estimate (i.e., predict) missing values based on existing data points. The `interpolate()` function fills missing values using linear interpolation, polynomial interpolation, or other interpolation techniques.

    # Interpolate missing values in a specific column
    df['Serious cases'].interpolate(inplace=True)
![filling-with-interpolation](./data-cleaning/filling-with-interpolation.png)

### 2. Removing duplicates



<!-- These are just a few examples of how Pandas can handle missing data. The choice of approach depends on the specific dataset, the nature of the missing values, and the analysis goals -->

<!-- 
### 👩🏾‍🎨 Practice: Describe JSON and XML Data... 🎯
In this exercise, you'll access data from sample APIs using your browser. With this, you'll have hands-on experience on JSON and XML data. Try the following in your browser.
1. Open your browser
2. copy and paste each of the url below in your browser <br>
    
    <aside>
    
    1. [https://api.unibit.ai/v2/stock/historical/?tickers=AAPL&accessKey=demo](https://api.unibit.ai/v2/stock/historical/?tickers=AAPL&accessKey=demo)
    2. [http://restapi.adequateshop.com/api/Traveler?page=1](http://restapi.adequateshop.com/api/Traveler?page=1)

    </aside>

3. Describe what each data from the APIs is all about in the padlett below
    **[https://padlet.com/curriculumpad/draw-the-building-blocks-b1yn0aft11t9n4ox](https://padlet.com/curriculumpad/draw-the-building-blocks-b1yn0aft11t9n4ox)**

> ➡️ In the next section, you'll be introduced to `data loading` and `data exploration` 🏙️.
 -->
