# Module 4: Pandas Challenge

-----------------
Table of Contents
-----------------

PyCitySchools Folder which contains

  - PyCity_Schools_Analysis.ipynb file. This is the main script.
 
  - PyCity_WrittenReport.docx file. This is the written report.

  
  - Resources folder with contains the .csv files used in the script

       - schools_complete.csv
    
       - students_complete.csv
    
    
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------

-------------------
Challenge Objective
-------------------

The objective of our analysis is to look at data of school students within a district from grade 9 to 12 and draw conclusions based on their performance, school type, school size and budget. The two .csv files is the source of raw data for this project. The actual analysis is perfomed in the .ipynb script, and results and conclusions are reported in the .docx file. 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

----------
References
----------

Here are the references used in my code:

1) To learn how to edit index column name in pandas data frame:

   https://stackoverflow.com/questions/29765548/remove-index-name-in-pandas

   https://stackoverflow.com/questions/18022845/how-to-get-set-a-pandas-index-column-title-or-name

   Code referenced:

   per_school_summary.index.name = None

   math_scores_by_grade.index.name = None

   reading_scores_by_grade.index.name = None


2) To learn how to format the the data frame output:

   https://stackoverflow.com/questions/38147447/how-to-remove-square-bracket-from-pandas-dataframe

   Code referenced:

   school_types = group_by_school["type"].unique().str.get(0)

   per_school_counts = group_by_school["size"].unique().str.get(0).astype(int)

   per_school_budget = group_by_school["budget"].unique().str.get(0).astype(int)


3) To learn how to change string with $ to float value and vice versa:

   https://stackoverflow.com/questions/3887469/python-how-to-convert-currency-to-decimal

   https://pbpython.com/currency-cleanup.html

   https://stackoverflow.com/questions/32464280/converting-currency-with-to-numbers-in-python-pandas

   Code referenced:

   school_spending_df['Per Student Budget'] = school_spending_df['Per Student Budget'].str.replace('$', '')

   school_spending_df = school_spending_df.astype({"Per Student Budget": "float64"})
   

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

