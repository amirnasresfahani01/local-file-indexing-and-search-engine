# HTML File Parser and Database Search Tool

## Overview
This project is a Python tool that parses HTML files, extracts their text content, stores the data in a MySQL database, and allows users to search files by their filename or content.

It is useful for indexing and searching large collections of HTML documents.

---

## Features
- Parse HTML files and extract text content
- Store extracted data in a MySQL database
- Search files by filename
- Search inside file content
- Highlight search results
- Clean terminal output using the **rich** library

---

## Project Structure

~~~
project/
│
├── main.py
├── README.md
└── requirements.txt
~~~

---

## Requirements

- Python 3.6 or higher
- MySQL Server

### Python Packages

- mysql-connector-python  
- lxml  
- rich  

---

## Installation

Clone the repository:

~~~bash
git clone https://github.com/amirnasresfahani01/local-file-indexing-and-search-engine.git
cd Local-File-Indexing-and-Search-Engine
~~~

Install dependencies:

~~~bash
pip install mysql-connector-python lxml rich
~~~

---

## Database Setup

Create a table named **wiki** in MySQL:

~~~sql
CREATE TABLE wiki (
    id INT AUTO_INCREMENT PRIMARY KEY,
    filename VARCHAR(255),
    file_size BIGINT,
    full_path TEXT,
    last_modified DATETIME,
    content LONGTEXT
);
~~~

---

## Database Configuration

Update the database connection settings in the script:

~~~python
connection = mysql.connector.connect(
    host="127.0.0.1",
    user="root",
    password="",
    database=""
)
~~~

---

## Usage

### Insert Data into Database

Parse HTML files from a directory and insert them into the database:

~~~python
directory_path = r'D:\DCRB with index'
parse_and_insert_data(directory_path)
~~~

This will parse HTML files, extract their text content, and store them in the **wiki** table.

---

### Run the Search Tool

~~~bash
python main.py
~~~

---

## Search Interface

- Enter a search term to find files by **filename** or **content**
- Type **exit** to quit the tool

Example:

~~~
Enter search term: machine learning
~~~

---

## Functions

**parse_html_file(file_path)**  
Extracts text content from an HTML file.

**create_indexes(connection)**  
Creates indexes in the database for faster search.

**parse_directory(directory_path, connection)**  
Parses HTML files in a directory and inserts them into the database.

**parse_and_insert_data(directory_path)**  
Handles the full parsing and insertion process.

**search_files_in_database(search_query, connection)**  
Searches the database for files matching the search query.

**display_search_results(search_query, filename_results, content_results)**  
Displays search results in a formatted table.

**highlight_search_query(text, query)**  
Highlights the searched keywords in the results.

---

## Contact

Email: amir.mza44@gmail.com  

LinkedIn:  
https://www.linkedin.com/in/amir-nasr-esfahani-584b90142

---
