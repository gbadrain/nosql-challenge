# UK Food Hygiene Ratings Database Analysis

## Overview
This project analyzes food hygiene ratings data provided by the UK Food Standards Agency to support the editors of *Eat Safe, Love* magazine in identifying areas of interest for future articles and reviews. The analysis is structured in three main components: database setup, database updates, and exploratory data analysis.

## Project Goals
1. Set up and explore the hygiene ratings database using MongoDB
2. Update the database with new data and apply requested modifications
3. Perform in-depth data exploration and analysis to generate actionable insights

## Repository Content

### Jupyter Notebooks
* **NoSQL_setup_starter.ipynb**:
  * Database setup and verification
  * Data import and exploration with PyMongo and Pretty Print
  * Connection establishment to the `uk_food` database and `establishments` collection

* **NoSQL_analysis_starter.ipynb**:
  * Exploratory analysis answering specific questions from the magazine editors
  * Queries include hygiene scores, RatingValue analysis, and location-based insights

### Data Files
* **establishments.json**: JSON dataset imported into MongoDB containing food hygiene ratings data

## Instructions

### Part 1: Database and Jupyter Notebook Set Up
1. Import the data into MongoDB using the Terminal:
   ```
   mongoimport --db uk_food --collection establishments --file establishments.json --jsonArray
   ```

2. Verify the database setup:
   * List databases and collections
   * Use `find_one` to inspect a sample document
   * Assign the `establishments` collection to a variable for further use

### Part 2: Update the Database
1. **Add New Restaurant**:
   * Insert a new halal restaurant, "Penang Flavours," into the `establishments` collection

2. **Update Fields**:
   * Assign the proper `BusinessTypeID` to "Penang Flavours"

3. **Data Clean-Up**:
   * Remove establishments in the Dover Local Authority
   * Convert latitude, longitude, and `RatingValue` fields to their appropriate numeric types

### Part 3: Exploratory Analysis
Analyze the data to answer the following key questions:

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a `RatingValue` greater than or equal to 4?

3. What are the top 5 establishments with a `RatingValue` of 5, sorted by the lowest hygiene score, nearest to "Penang Flavours"?

4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results in descending order and display the top ten.


## Results
The analysis provides insights into food establishment hygiene scores across the UK, highlighting potential areas of concern and interest for *Eat Safe, Love* magazine's future articles.

## Sources of Help
* MongoDB Documentation
* *Eat Safe, Love* editors' action items
* YouTube tutorials on MongoDB and Python integration
* Microsoft Copilot for problem-solving

## References
The dataset was provided by the UK Food Standards Agency for analysis. All operations and queries were performed in compliance with ethical and legal standards.

## Contact
[Gurpreet Singh Badrain]
