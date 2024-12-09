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


