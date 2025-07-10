# **🗃️ RDBMS 101: Introduction to Relational Databases**

**💡 What Is an RDBMS?**

**RDBMS = Relational Database Management System**

It is software that helps you **store, manage, and organize data in tables** — just like a super-powered spreadsheet.

🧠 Think of an RDBMS like a **digital filing cabinet**, where each **drawer is a table**, and each **folder is a row of data**.

**📊 What Makes It “Relational”?**

In an RDBMS:

- **Data is stored in tables**
- **Tables can be linked together** through relationships (using IDs)
- You can **query** data using a language called **SQL**

✨ “Relational” = Tables can reference each other like **friends in a contact list**.

**🧱 Tables, Rows, and Columns**

|**Term**|**What It Is**|**Analogy**|
| :- | :- | :- |
|**Table**|A group of related data|A spreadsheet|
|**Row**|A single record (entry)|A line in the spreadsheet|
|**Column**|A specific type of data (name, age, etc.)|A labeled column in Excel|
|**Primary Key**|A unique ID for each row|Student ID, Product ID|
|**Foreign Key**|Links to another table’s Primary Key|“Student ID” in another table|

**

**📁 Real-World Example: Student Database**

**students Table:**

|**student\_id**|**name**|**age**|
| :- | :- | :- |
|1|Aung|19|
|2|Sarah|20|

**courses Table:**

|**course\_id**|**title**|
| :- | :- |
|101|Intro to AI|
|102|Web Dev Basics|

**enrollments Table (relationship table):**

|**student\_id**|**course\_id**|
| :- | :- |
|1|101|
|2|101|
|2|102|

This is how we represent **many-to-many relationships**:\
One student can enroll in many courses, and one course can have many students.

**

**🛠️ What Does an RDBMS Do?**

|**Feature**|**Description**|
| :- | :- |
|**Store**|Saves large amounts of structured data|
|**Retrieve**|Get specific data quickly|
|**Query**|Ask questions using SQL|
|**Relate**|Link data across tables|
|**Secure**|Manage access and permissions|
|**Scale**|Handle data for small apps or large platforms|

Popular RDBMS tools: **MySQL, PostgreSQL, SQLite, Microsoft SQL Server**

**🧩 Introduction to SQL (Structured Query Language)**

SQL is how you **talk to a database**.

**📌 Basic SQL Examples**

-- Select all rows from a table

SELECT \* FROM students;

-- Select only names from students

SELECT name FROM students;

-- Filter: Get students aged 20ooo

SELECT \* FROM students WHERE age = 20;

-- Join two tables

SELECT students.name, courses.title

FROM students

JOIN enrollments ON students.student\_id = enrollments.student\_id

JOIN courses ON courses.course\_id = enrollments.course\_id;

**🧪 Hands-On Activity (No Code Required)**

Simulate a database using **Google Sheets** or **Notion Database**

1. Create a “Students” table
1. Create a “Courses” table
1. Link them using IDs in a third “Enrollments” table
1. Try writing questions (queries) in plain English:
   1. “Which students are enrolled in Intro to AI?”
   1. “How many courses is Sarah taking?”

**🧠 Why Learn RDBMS?**

|**Benefit**|**Real-World Impact**|
| :- | :- |
|Organize structured data|Websites, apps, banks, hospitals|
|Work with APIs and backends|Store user info, products, orders|
|Power your projects|Blogs, e-commerce, dashboards|
|Learn key industry skill|Used in nearly every business and tech|

**

**🔧 Beginner-Friendly Tools**

|**Tool**|**Purpose**|
| :- | :- |
|**SQLite**|Lightweight local database|
|**MySQL**|Popular open-source RDBMS|
|**PostgreSQL**|Powerful, developer-friendly RDBMS|
|**DB Fiddle**|Test SQL queries in the browser|
|**Beekeeper Studio**|GUI for databases|

**💬 Final Thought**

“A database isn’t just where data lives — it’s how data makes sense.”

Learning RDBMS helps you **organize**, **query**, and **relate** data — which powers almost every modern software system.



