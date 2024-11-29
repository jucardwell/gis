---
title: Assignment 1
layout: default
parent: Assignments
nav_order: 1
---



<style>
div.blue { background-color:#e0f0ff; padding: 10px 10px 3px 10px;}
</style>

------------------------------------------------------------------------
# Assignment 1

In this assignment, you will read in a file, practice some basic data
manipulation, and make a graph. You will be performing all your work
within an R Markdown document for this assignment. You will be working
with North Carolina countywide population projections provided by the
North Carolina Office of State Budget and Management
(<https://www.osbm.nc.gov/facts-figures/population-demographics/state-demographer/countystate-population-projections/population-overview>).
Make sure each line of code has a descriptive comment. 

[**Download the Data Here**](https://drive.google.com/uc?export=download&id=1n931oVVyQPzLfNlSBbwGTWppLXlpLq1H)
------------------------------------------------------------------------

### Create a new R Markdown document

1.  If RStudio is open, close it and do not save your environment. Open
    RStudio and make sure that your environment is empty, then choose
    File | New File | R Markdown. *Note: to clear your Environment, find
    the button that looks like a broom in the Environment tab!*

    In the popup window, enter “Assignment \#1” for the title and for
    author, enter your name. Make sure that the type (on the left) is
    Document and the Default Output Format is HTML.

    Note that the new R Markdown document should have populated the
    “header” section to include the information you entered. For
    example, mine looks like this:

<style type="text/css">
.indent {
 margin-left: 40px;
}
</style>

    ---
    title: "Assignment #1"
    author: "Julia Cardwell"
    date: "5/1/2023"
    output: html_document
    ---

1.  Save your .RMD file using the following naming convention:

-   **Lastname**\_GEOG215\_Assg**1**.Rmd
-   For example, Julia’s file would be: **Cardwell\_GEOG215\_Assg1.Rmd**

### Read in and Summarize the Data

1.  Add a code chunk at the top of your .Rmd. Load the tidyverse library

2.  Add a **third-level heading** to your R Markdown file named, “Read
    in Data”. Below this heading, add a code chunk. In the chunk, use a
    relative file path to read in (using the `read_csv()` command) the
    file named “nc\_population\_projections.csv” and assign it to an
    object called `nc_pop`.

3.  Under the code chunk you just created, insert a **third-level
    heading** to your R Markdown file named, “Data Preparation and
    Summary”. Create an object called `nc_pop_simplified` that only
    contains the following variables: `pop_2010`, `pop_2020`,
    `pop_2030`, `pop_2040`, `pop_2050`.

4.  Using in-line code, write a sentence (in plain text underneath the
    code chunk) that describes the number of rows and the number of
    columns in `nc_pop_simplified`. You must use a command to complete
    this task, not simply write the correct answer.

### Create a Plot

1.  Under the code chunk you last created, insert a **third-level
    heading** to your R Markdown file named “Plot”.

2.  Write a command to create a histogram of all county values in the
    `pop_2050` column.

### Calculate State-Level Values

After examining the dataset, you have probably noticed that each row
represents a county in North Carolina. It is often useful to examine the
“study region” as a whole (in this case, the full state). We will now
aggregate the county-level data to the state-level.

1.  Under the code chunk you last created, insert a **third-level
    heading** to your R Markdown file named “Aggregating data”

2.  Write a command that creates a new object called `state_summary`
    that gets the sum of each column except `County`.

3.  Add a new column to the `state_summary` object called
    `overall_change`. Use the `mutate()` command to fill this column
    with the statewide population change from 2010-2050

4.  In plain text below the code chunk, explain why we would get an
    error if we try to take the sum of the `County` variable. In that
    same plain text, add in-line code that prints the statewide
    population change from 2010-2050.

------------------------------------------------------------------------

### Deliverables

Upload your .Rmd and .html files to Canvas.
