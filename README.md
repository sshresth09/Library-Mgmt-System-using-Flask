# Library-Mgmt-System-using-Flask

## Setup
1. Clone the repository.

2. Install libraries
```
pip install requirements.txt
```

3. Create a MySQL database named lbms and set up the required tables using the SQLAlchemy model structure.

4. Configure SQLAlchemy Database URL
```
app.config["SQLALCHEMY_DATABASE_URI"] = "mysql+pymysql://root:root@localhost:3306/table_name"
```

5. Run the python file
```
python app.py
```

## Design
### 1. Framework
Flask: Lightweight, flexible, and well-suited for building small to medium-sized web applications. It allows easy routing and rendering of templates.

### 2. Database Integration
<ul>
<li>SQLAlchemy: Used as the Object-Relational Mapper (ORM) to interact with the MySQL database. It simplifies database operations and improves code maintainability.

<li>MySQL: Chosen for its reliability, scalability, and wide community support.
</ul>

### 3. Database Tables
<li>students: Tracks student information like name, department, contact, gender, and registration date.

<li>books: Manages the library's inventory of books with title, edition, and author details.

<li>borrow: Stores records of borrowed books, including the student's name, book title, token number, and due date.

<li>b_return: Keeps records of returned books, including the student’s name, book title, token number, and charges (if any).

### 4. Routing
Routes are designed to follow REST principles:

<li>/: Homepage displaying all borrowed books.

<li>/insert: Handles adding new students.

<li>/book: Handles adding new books to the inventory.

<li>/borrow_book: Facilitates borrowing of books by students.

<li>/return_book: Facilitates returning books and recording charges.
