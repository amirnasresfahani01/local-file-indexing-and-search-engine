# HTML File Parser and Database Search Tool

## Overview

This project is a Python-based tool designed to:

- Parse **HTML files** and extract their text content
- Store the extracted content in a **MySQL database**
- Provide a **search interface** to find files by **filename or content**

It is useful for indexing large collections of HTML documents and quickly searching through them.

---

# Features

- HTML parsing using **lxml**
- MySQL database storage
- Search by **file name**
- Search by **file content**
- Highlighted search results
- Clean terminal interface using **rich**

---

# Project Structure
project/
│
├── main.py
├── README.md
└── requirements.txt

---

# Requirements

- Python **3.6+**
- MySQL Server

### Python Packages

- mysql-connector-python
- lxml
- rich

---

# Installation

## 1. Clone the repository

```bash
git clone https://github.com/amirnasresfahani01/html-parser-search-tool.git
cd html-parser-search-tool
```

2. Install dependencies

### 2. Install dependencies
pip install mysql-connector-python lxml rich

Database Setup

Create a database in MySQL and a table named wiki.
CREATE TABLE wiki (
    id INT AUTO_INCREMENT PRIMARY KEY,
    filename VARCHAR(255),
    file_size BIGINT,
    full_path TEXT,
    last_modified DATETIME,
    content LONGTEXT
);



