# colleen547-sql-challenge

<b>Employee SQL Database: A Mystery in Two Parts</b>
<div style="text-align:center"><img src="static/images/Relations_SQL.png" width="500" height="300"/></div>

<b>BACKGROUND SCENARIO</b><br>
Imagine it's a beautiful spring day, and it's been two weeks since you have been hired as a new data engineer at Pewlett Hackard. Your first major task is a research project on employees of the corporation from the 1980s and 1990s. All that remains of the database of employees from that period are six CSV files.
<br>

Tables were designed to hold data in the CSVs, import the CSVs into a SQL database, and answer questions about the data. In other words, you will perform:


   1.) Data Engineering


   2.) Data Analysis


<b>Data Modeling</b>
- Inspect the CSVs and sketch out an ERD of the tables. Feel free to use a tool like http://www.quickdatabasediagrams.com.

<b>Data Engineering</b>
- Use the information you have to create a table schema for each of the six CSV files. Remember to specify data types, primary keys, foreign keys, and other constraints.

  - For the primary keys check to see if the column is unique, otherwise create a composite key. Which takes two primary keys in order to uniquely identify a row.
  - Be sure to create tables in the correct order to handle foreign keys.



- Import each CSV file into the corresponding SQL table. Note: be sure to import the data in the same order that the tables were created and account for the headers when importing to avoid errors.



<b>Data Analysis</b>
Once you have a complete database, the following were created:


   1.) Lists the following details of each employee: employee number, last name, first name, sex, and salary.


   2.) Lists first name, last name, and hire date for employees who were hired in 1986.


   3.) Lists the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.


   4.) Lists the department of each employee with the following information: employee number, last name, first name, and department name.


   5.) Lists first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."


   6.) Lists all employees in the Sales department, including their employee number, last name, first name, and department name.


   7.) Lists all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.


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

