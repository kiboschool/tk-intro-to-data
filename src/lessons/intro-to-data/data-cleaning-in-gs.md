# ♻️ Data Cleaning 
In data science, `unclean` data refers to a dataset that contains errors, inconsistencies, or inaccuracies, making it unsuitable for analysis without preprocessing. Such data may have missing values, duplicate entries, incorrect formatting, inconsistent naming conventions, outliers, or other issues that can impact the quality and reliability of the data. These problems can arise from various sources, such as... 

- Data entry errors
- Measurement inaccuracies
- Technical issues during data collection or storage. 

Cleaning the data involves identifying and addressing these issues to ensure that the dataset is accurate, complete, and reliable before further analysis or modeling takes place.

<aside>

**_Definition..._**

**_Data cleaning_** involves the process of identifying and correcting errors, inconsistencies, and missing values in a dataset to ensure its accuracy and reliability.
</aside>

Data cleaning aims to improve the integrity, completeness, and consistency of the data. When cleaning a data, our goal will be to produce a clean and reliable dataset that is ready for further analysis. By investing time and effort into data cleaning, we can improve the accuracy and credibility of our analysis results, leading to more robust and reliable insights. To understand this more, we'll be looking at the following.

## Data cleaning with Google Sheet ♻️

In GS, data cleaning can involve tasks such as removing duplicate values, correcting misspellings, handling missing data by filling in or deleting the values, and formatting data appropriately. GS provides us with various built-in functions and tools, such as filters, conditional formatting, and formulas, that can help with data cleaning tasks. 

When we carry out data cleaning, we can improve the quality of our datasets and ensure that the data is ready for further analysis or visualization. To have an understanding of how to clean a dataset, we'll be looking at 3 things for this lesson. 


<aside>

- Handling missing data
- Removing duplicate data values 
- Fixing #VALUE! error
- Conditional formatting

</aside>


### 1. Handling missing data
Missing data is one of the most frequently occuring problems you can face as a data scientist. Watch the next video to have an idea of how important it is to understand this problem, and possible causes.

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/BqtTcOtkp6Y" title="Web Scrapping Intro" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

As a data scientist, there are many ways of dealing with missing values in a data. For this lesson, we'll be looking at 4 different techniques of handling missing data -  _dropping, filling with constant, filling with statistics, and _interpolation_. 

<aside>

- Watch the next video 📺. 
- Pause and practice along with the tutor.
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/H0tRB7fgM4VI8" title="Sample Data Science Project" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 1px solid grey;"></iframe></div>

#### 2. Removing Duplicates

Duplicate data are rows or records within a dataset with similar or nearly identical values across all or most of their attributes.
This can occur due to various reasons, such as data entry errors, system glitches, or merging data from different sources. As a data scientist, there are number of ways to handle duplicate data in a small or large dataset.
<aside>

- Watch the next video 📺. 
- Pause and practice along with the tutor.
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/hS9kENtjaxI?si=QZwZYyxH-DNeR3Q-" title="Removing duplicate data" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 1px solid grey;"></iframe></div>

<aside>

**A brief recap of removing duplicates in a data...**
- Google Sheets has a built-in function called `UNIQUE` to remove duplicate data.
- To use the `UNIQUE` function, select a cell below or to the right of the data, type "_unique_" followed by the range of data enclosed in parentheses, and press Enter.
- The `UNIQUE` function outputs the same list without duplicates, starting from the cell where the formula is entered and continuing below.
- To convert the output to a static format, copy the data, right-click, select "Paste special" and choose "Paste values."
- The `UNIQUE` function considers duplicates **ONLY** if every value in the row or column is duplicated; it does not consider duplicates across different columns.
</aside>

#### 3. #VALUE! Error
The `#VALUE!` error in Google Sheets is caused by attempting to perform calculations or operations involving cells containing incompatible data types, such as trying to add text to a numerical calculation or using dates in an inappropriate context.

<aside>

- Watch the next video 📺. 
- Pause and practice along with the tutor.
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/zXEbfvVUa9A?si=iRD5G8PkjXT5E_wb" title="Fixing Value Error" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 1px solid grey;"></iframe></div>

<aside>

**A brief recap of fixing the `#VALUE!` error...**
- Google Sheets can display a `#VALUE!` error when a cell contains text instead of a number, disrupting calculations.
- To identify and fix text entries causing the error, one method is to use the `is_text` function in an additional column to highlight problematic cells.
- Alternatively, formulas like `SUM` or `AVERAGE` can handle text entries without throwing errors, ensuring calculations proceed smoothly.
- Hidden characters, such as spaces, can also trigger the error. Manually deleting or using functions like `TRIM` can resolve this issue.
- Dates can also cause `#VALUE!` errors if they're not recognized properly. Using functions like `ISDATE` or conditional formatting can help identify and fix invalid dates.
</aside>

#### 4. Conditional Formatting
Conditional formatting is used in Google Sheets, as well as other spreadsheet software, to visually highlight and emphasize data based on specific conditions or criteria.

<aside>

- Watch the next video 📺. 
- Pause and practice along with the tutor.
</aside>

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/W7wjXGzB4hs?si=rLfvNkHd4Fmcwrk_" title="Web Scrapping Intro" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 2px solid grey;"></iframe></div>

<aside>

**A brief recap on conditional formatting...**
- We selected the column to be formatted and specified the range in the conditional formatting dialog.
- A custom formula is entered, starting with `=` to compare values from a different column (e.g., if B2 equals "Joan").
- It is important to use quotes for strings and fixing the column reference in the formula using a `$` to prevent it from moving when applied to different cells.
</aside>



<!-- <aside>

**A brief recap of data cleaning using Excel...**
In the video above, we have covered the following techniques in data cleaning

- **Separating Text** - separating multiple text in a column into different cells.
- **Removing Duplicates** - removing duplicate data with `unique()` formula and `replace` feature.
- **Letter cases** - using `proper()` to remove inconsistent capital letters.
- **Spacing fixes** - removing spacing with `trim()` formula.
- **Splitting text** - flash fill to automatically separate data such as city and country
- **Percentage formats** - changing numbers to percentages
- **Text to Number** - text to values for further calculations
- **Removing Blank Cells** - removing blank cells from a dataset.
</aside> -->


## Smart CleanUp in GS
With GS Smart Cleanup feature, we can do many things in an easier manner. Let's look at two important functionalities of this feature...
- **Finding Problems**: It takes a look at your data set, and tries to find out if there could be any problems in that dataset. For example, are there any duplicates in that data set? Is there anything that might be spelled incorrectly? So it gives you a chance to fix your dataset before you analyze it. 
- **Statistics**: Smart Cleanup can help take a look at a column, and gives some statistics based on that column.

> 📺 Watch the video below on using Smart Cleanup and practice along.

<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.youtube.com/embed/tihtx5AS_k8?si=xTapE5uupvEFl1cq" title="Sample Data Science Project" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 1px solid grey;"></iframe></div>
<aside>


**_Chapter summary...✍🏾_**

_Data cleaning_ involves the process of identifying and rectifying errors, inconsistencies, and missing values in a dataset. We can start by examining the data for any obvious mistakes or inconsistencies and then use GS's functions and tools to clean the data. This may include removing duplicates, handling missing values, correcting formatting issues, and ensuring data consistency and accuracy. 

GS provides features such as filters, conditional formatting, find and replace, and formula-based operations that can assist in performing these cleaning tasks. 

**_It is important to approach data cleaning systematically and document the steps taken to maintain transparency and reproducibility_**.
</aside>

### 👩🏾‍🎨 Practice: Clean the smell... 🎯
A smaller sample of the global COVID-19 dataset is provided **[here](https://docs.google.com/spreadsheets/d/1FxxX9wSUMJwsa0xuw8EALSDG4eQcQpxRDCRpAIeDXUY/edit?usp=sharing)** for this exrcise.
1. Create a copy of the dataset for your own use. 
2. Explore the dataset to have a sense of what the it represent.
3. By leveraging your data cleaning skills, attempt the following...
    - Remove duplicate data if exist
    - Handle blank space
    - Convert the column from text to number
    - Implement other cleaning techniques of your choice
4. Submit this exercise using **[this form](https://docs.google.com/forms/d/e/1FAIpQLSe6D2X-nK8KpDzRUqq5-aci-sbFQTXrFv1wtZBqaLFrYu8pjg/viewform?usp=sharing)**.

</aside>


> 👉🏾 Next, we'll deep dive into creating cool visualization with Excel.
