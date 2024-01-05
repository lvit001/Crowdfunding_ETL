# Crowdfunding_ETL


# Instructions
The instructions for this mini-project are divided into the following subsections:
  1. Create the Category and Subcategory DataFrames
  2. Create the Campaign DataFrame
  3. Create the Contacts DataFrame
  4. Create the Crowdfunding Database

# [Jupyter Notebook File](https://github.com/lvit001/Crowdfunding_ETL/blob/main/ETL_Mini_Project_LVitaioli_HShoberg.ipynb)
  
# Create the Category and Subcategory DataFrames
1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
  A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
  A "category" column that contains only the category titles

2. Export the category DataFrame as [category.csv](https://github.com/lvit001/Crowdfunding_ETL/blob/main/Resources/category.csv) and save it to your GitHub repository.

3. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
  A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
  A "subcategory" column that contains only the subcategory titles

4. Export the subcategory DataFrame as [subcategory.csv](https://github.com/lvit001/Crowdfunding_ETL/blob/main/Resources/subcategory.csv) and save it to your GitHub repository.

# Create the Campaign DataFrame
1. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
  The "cf_id" column

  The "contact_id" column
  
  The "company_name" column
  
  The "blurb" column, renamed to "description"
  
  The "goal" column, converted to the float data type
  
  The "pledged" column, converted to the float data type
  
  The "outcome" column
  
  The "backers_count" column
  
  The "country" column
  
  The "currency" column
  
  The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
  
  The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
  
  The "category_id" column, with unique identifi cation numbers matching those in the "category_id" column ofthe category DataFrame
  
  The "subcategory_id" column, with the unique identifi cation numbers matching those in the "subcategory_id"column of the subcategory DataFrame

2. Export the campaign DataFrame as [campaign.csv](https://github.com/lvit001/Crowdfunding_ETL/blob/main/Resources/campaign.csv) and save it to your GitHub repository.

# Create the Contacts DataFrame
1. Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Exceldata:

  - Option 1: Use Python dictionary methods.
  - Option 2: Use regular expressions.

2. If you chose Option 1, complete the following steps:

  Import the contacts.xlsx file into a DataFrame.
  _Note: when exporting this file, the initial code that was provided needed to be changed for the export to work correctly. `header=2` was updated to `header=3` as that was when the header row began_

  Iterate through the DataFrame, converting each row to a dictionary.

  Iterate through each dictionary, doing the following:

  Extract the dictionary values from the keys by using a Python list comprehension.

  Add the values for each row to a new list.

  Create a new DataFrame that contains the extracted data.

  Split each "name" column value into a first and last name, and place each in a new column.

  Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

3. If you chose Option 2, complete the following steps:

  Import the contacts.xlsx file into a DataFrame.

  Extract the "contact_id", "name", and "email" columns by using regular expressions.
  _For the email column, had help with the regex code for extracting emails from [here](https://stackoverflow.com/questions/42407785/regex-extract-email-from-strings)._

  Create a new DataFrame with the extracted data.

  Convert the "contact_id" column to the integer type.

  Split each "name" column value into a first and a last name, and place each in a new column.

  Clean and then export the DataFrame as [contacts.csv](https://github.com/lvit001/Crowdfunding_ETL/blob/main/Resources/contacts.csv) and save it to your GitHub repository.

# Create the Crowdfunding Database

  1. Inspect the four CSV files, and then sketch an [ERD](https://github.com/lvit001/Crowdfunding_ETL/blob/main/Resources/ERD.png) of the tables by using QuickDBD(http://www.quickdatabasediagrams.com).
  2. ![image](https://github.com/lvit001/Crowdfunding_ETL/assets/140283164/4ee45501-f802-4818-b03c-790e36415994)
  3. Use the information from the ERD to create a table schema for each CSV file.
      Note: Remember to specify the data types, primary keys, foreign keys, and other constraints.
  4. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHubrepository.
  5. Create a new Postgres database, named crowdfunding_db.
  6. Using the [database schema](https://github.com/lvit001/Crowdfunding_ETL/blob/main/Resources/crowdfunding_db_schema.sql), create the tables in the correct order to handle the foreign keys.
  7. Verify the table creation by running a SELECT statement for each table.
  8. ![image](https://github.com/lvit001/Crowdfunding_ETL/assets/140283164/d5c5dd86-eeb7-4c2f-8cf5-69e2a3d7483e)
  9. Import each CSV file into its corresponding SQL table.
  10. Verify that each table has the correct data by running a SELECT statement for each.
  11. ![image](https://github.com/lvit001/Crowdfunding_ETL/assets/140283164/8f614178-2f93-4618-b1a4-6c6e892e7c9a)
  12. ![image](https://github.com/lvit001/Crowdfunding_ETL/assets/140283164/b97d6892-b2de-42c7-b01d-19a0e379c0d6)
  13. ![image](https://github.com/lvit001/Crowdfunding_ETL/assets/140283164/ac7e6a53-520e-43ac-94b5-ab6878d492e2)
  14. ![image](https://github.com/lvit001/Crowdfunding_ETL/assets/140283164/8901767d-edad-48ef-b8e0-268136e925e8)





