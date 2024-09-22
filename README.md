# Netflix Data Analysis Project

## Project Overview
This project performs data analysis on the Netflix dataset to extract insights related to the types of content available on the platform, the directors, cast members, ratings, and more. The project involves:
- Loading and cleaning data from a CSV file.
- Storing the data in a relational database (SQL Server).
- Running SQL queries to analyze the data.
  
The goal is to improve the understanding of content distribution, duplication issues, and trends in Netflix's catalog.

## Files in This Project
1. **`netflix_titles.csv`**: Contains metadata of Netflix shows such as:
   - `show_id`: Unique identifier for each show.
   - `type`: Whether the show is a Movie or a TV Show.
   - `title`: Name of the show.
   - `director`: The director of the show.
   - `cast`: The main cast members.
   - `country`: Country of origin.
   - `release_year`: Year the show was released.
   - `rating`: Content rating of the show.
   - `duration`: Length of the show (in minutes or seasons).
   - `listed_in`: Genres or categories the show is listed in.

2. **`netflix_raw.sql`**: This SQL script creates a table for the raw Netflix data, defining the schema used for storing the data in a relational database.

3. **`netflix_data_analysis.sql`**: Contains SQL queries to analyze the Netflix data, including:
   - Removing duplicate records.
   - Handling foreign characters in titles.
   - Filtering the data by `show_id`, `title`, and `type`.

4. **`netflix_data_extract.py`**: Python script to extract the data from the CSV file and load it into a SQL Server database using `pandas` and `SQLAlchemy`. It also performs initial data checks such as handling missing values.

## How to Run This Project

### Prerequisites
- Python 3.x
- Pandas (`pip install pandas`)
- SQLAlchemy (`pip install sqlalchemy`)
- Microsoft SQL Server (or any compatible SQL database)
- ODBC driver for SQL Server (`ODBC DRIVER 17 FOR SQL SERVER`)

### Steps

1. **Set up the database**:
   - Create a database using Microsoft SQL Server.
   - Run the `netflix_raw.sql` script to create the `netflix_raw` table.

2. **Load the data**:
   - Use the `netflix_data_extract.py` Python script to load the data from `netflix_titles.csv` into the SQL database.

3. **Analyze the data**:
   - Execute the SQL queries in `netflix_data_analysis.sql` to perform the analysis, such as detecting duplicates and filtering data.

### Key Insights from Analysis
- Identified and removed duplicate records in the Netflix dataset.
- Filtered shows based on different criteria (e.g., `show_id`, `title`, `type`).
- Provided a foundation for further analysis, such as exploring trends in Netflix’s content over time or examining patterns in ratings and genres.

