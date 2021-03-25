# colleen547-sql-challenge

<b>Employee SQL Database: A Mystery in Two Parts</b><br>
In this project, tables were designed to hold data in CSVs, the CSVs were imported into a SQL database, and questions were answered about the data by performing the following steps:<br> 


   1.) Data Modeling

   2.) Data Engineering

   3.) Data Analysis

<img src="static/images/Relations_SQL.png" width="500" height="400"/><img style="float:right"></div>

<b>BACKGROUND SCENARIO</b><br>
Imagine you have just been hired as a new Data Engineer and your first major task is a research project on employees of the corporation from the 1980s and 1990s, but all that remains of the database of employees from that period are six CSV files.
<br>

<b>Data Modeling</b>
- The CSVs were inspected and an ERD of the tables was sketched out using http://www.quickdatabasediagrams.com.

<b>Data Engineering</b>
- Using the information obtained, a table schema was created for each of the six CSV files including specifying data types, primary keys, foreign keys, and other constraints.

  - For the primary keys, columns were checked to see if the column is unique, otherwise a composite key, which takes two primary keys in order to uniquely identify a row, was created.
  - Care was taken to create tables in the correct order to handle foreign keys.



- Next each CSV file was imported into the corresponding SQL table, in the same order that the tables were created as well as by accounting for headers, to avoid errors.



<b>Data Analysis</b>
Once the database was complete, the following were created:


   1.) The following details of each employee: employee number, last name, first name, sex, and salary.


   2.) First name, last name, and hire date for employees who were hired in 1986.


   3.) The manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.


   4.) The department of each employee with the following information: employee number, last name, first name, and department name.


   5.) First name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."


   6.) All employees in the Sales department, including their employee number, last name, first name, and department name.


   7.) All employees in the Sales and Development departments, including their employee number, last name, first name, and department name.


In descending order, list the frequency count of employee last names, i.e., how many employees share each last name.



<b>Bonus (Optional)</b>
As you examine the data, you are overcome with a creeping suspicion that the dataset is fake. You surmise that your boss handed you spurious data in order to test the data engineering skills of a new employee. To confirm your hunch, you decide to take the following steps to generate a visualization of the data, with which you will confront your boss:


   1.) Import the SQL database into Pandas. (Yes, you could read the CSVs directly in Pandas, but you are, after all, trying to prove your technical mettle.) This step may require some research. Feel free to use the code below to get started. Be sure to make any necessary modifications for your username, password, host, port, and database name:
from sqlalchemy import create_engine
engine = create_engine('postgresql://localhost:5432/<your_db_name>')
connection = engine.connect()

Consult SQLAlchemy documentation for more information.


If using a password, do not upload your password to your GitHub repository. See https://www.youtube.com/watch?v=2uaTPmNvH0I and https://help.github.com/en/github/using-git/ignoring-files for more information.


   2.) Created a histogram to visualize the most common salary ranges for employees.


   2.) Created a bar chart of average salary by title.


<b>Epilogue</b><br>
Evidence in hand, you march into your boss's office and present the visualization. With a sly grin, your boss thanks you for your work. On your way out of the office, you hear the words, "Search your ID number." You look down at your badge to see that your employee ID number is 499942.

