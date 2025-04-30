📝 Description:
Built an end-to-end ETL pipeline that extracts movie data from The Movie Database (TMDB) API, cleans and transforms it using Python and Pandas, and loads it into a SQLite database for structured analysis.
The pipeline automates data ingestion, handles nested JSON structures (like genre IDs), performs normalization (splitting movies and genres into separate relational tables), and ensures schema-ready data for analytics and reporting.

Used SQL to derive key insights such as:

Top 10 most popular movies

Average rating per language

Most common genres

Year-wise movie release trends

Genre-specific performance using joins and aggregations

✅ Tools & Technologies Used:
Python: Data extraction, cleaning, transformation

Requests: API integration with TMDB

Pandas: Data wrangling and preparation

SQLAlchemy: Database connection & loading

SQLite: Lightweight local database

SQL: Data analysis using joins, grouping, filtering, and window functions

📊 Data Model:
movies: Stores core movie information (title, release date, rating, etc.)

movie_genres: Many-to-many bridge table mapping movies to genres



📘 README Overview (Up to SQL Queries)
🎯 Project Objective
To build an end-to-end data engineering pipeline that:

Extracts movie data from the TMDB API

Transforms and normalizes it using Python and Pandas

Loads it into a SQLite database

Uses SQL for analytical querying (joins, aggregations, time-series)

🛠️ Tech Stack

Component	Tool
Data Source	TMDB Public API
Programming	Python 3
Libraries	requests, pandas, sqlalchemy
Database	SQLite
Query Language	SQL
Platform	Google Colab / Local Machine
🧱 Architecture Diagram (Conceptual)
pgsql
Copy
Edit
           +--------------------+
           |  TMDB API (JSON)   |
           +--------------------+
                     |
                [Extract]
                     |
           +--------------------+
           |  Python (ETL Code) |
           +--------------------+
                     |
                [Transform]
                     |
           +--------------------+
           |   Cleaned Data     |
           | (movies, genres)   |
           +--------------------+
                     |
                 [Load]
                     |
           +---------------------+
           | SQLite DB (movies.db)|
           +---------------------+
                     |
                [Query using SQL]
                     ↓
            Insights & Reports


            
📦 Data Flow
extract_movies() — pulls raw movie JSON from TMDB API

transform_movies() — flattens JSON, explodes genre arrays, cleans columns

load_movies() — loads cleaned data into two relational tables:

movies

movie_genres



📊 Key SQL Queries Practiced
Top 10 most popular movies

Movies released after 2020

Count of movies per year

Average rating by language

Most common genres (using joins)

Movies with above-average popularity per genre

Top movie per year (using window functions)



✅ How to Run the Project (Colab or Local)
Get your TMDB API key from https://developer.themoviedb.org

Paste your key into the API_KEY variable

Run the ETL code cells step-by-step in a Colab notebook or script

Explore the database using SQL queries with pandas.read_sql()


