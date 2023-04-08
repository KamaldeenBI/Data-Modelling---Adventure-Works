# Data-Modelling on MySQL, PowerBI---Adventure-Works

## COMPANY OVERVIEW
Adventure works is a large, multinational manufacturing company that produces and distributes bycycles, parts, and assessories for commercial markets in North America, Europe and Asia. The company employs 500 workers. 

## PROBLEM STATEMENT
The manufacturing company keeps tables of data for 6 departments in their database namely, "Production", "Person", "Human Resources", "Purchasing" and "Sales". There is need to define and analyze all the different data the business has collected and produced over time, as well as defining and creating relationships between those bits of data and tables generally.

## DATA SOURCING AND QUERYING
github.com/Microsoft/sql-server-samples/releases/tag/adventureworks

Extracted the Adventure Works BAK file from the above primary source into MySQL Server, by connecting it into Microsoft SQL Server program files folder
![Screenshot (309)](https://user-images.githubusercontent.com/108130729/230701743-3dc2eff9-5709-4f24-9628-28ce1afa5c88.png)

Which after some configurations on the MySQL server, created a new Database
![Screenshot (314)](https://user-images.githubusercontent.com/108130729/230702212-361339ca-072b-4522-b55f-b10dd82abfb5.png)

The next step in this sequence was to connect to MySQL database from PowerBI with the appropriate credentials of the server name and database name which in turn returns all corresponding tables in the queried database. The tables were connected to "Import" as against "DirectQuery" if we needed to the resultant data in all tables to update in real time, but for this project, we have a historical stipulated span of four years we are working with.
![Screenshot (312)](https://user-images.githubusercontent.com/108130729/230702335-cf18ebe8-9caf-448f-a2e9-7c71d7111140.png)

![Screenshot (318)](https://user-images.githubusercontent.com/108130729/230702866-f07f58ac-b244-44f0-829c-cc56b40bde87.png)
Below is the resultant PowerQuery editor when I hit the "transform data" instead of loading directly into Power BI

I did some data wrangling mainly with the PowerQuery Editor to structure all of the tables by dropping 'irrelevant for project purpose columns' in most tables, Merging some complementary columns into one, replacing values initials, shorts into more comprehensive content for analysis purposes, Changed to appropriate data types where necessary and finally removed duplicates and errors carefully in each table. All these necessities were satisfied in other to have a less complex subsequent data modeling exercise.
![Screenshot (319)](https://user-images.githubusercontent.com/108130729/230702882-94f716c2-63f5-4319-9dd6-a6c813545920.png)

After extensive tranformaton and structuring of the data, I proceeded to load the data into PowerBI
![Screenshot (325)](https://user-images.githubusercontent.com/108130729/230703600-d59fc5b8-8ef1-4957-8265-8355a81d9369.png)

One of the three work Interfaces of PowerBI is the model view. The Model view shows all of the tables, columns, and relationships in a model. This view can be especially helpful when a model has complex relationships between many tables. The built in Intellisense in PowerBI tries to help connect percieved related tables but the Adventure Works tables looked more complicated than what it can maneuver.

It created series of one-to-many, many-to-many relationships which some met project objectives and some didn't and would then be re-established.
Many tables pertaining to the Human Resources, Sales and Purchasing departments as shown below were isolated and the Intellisense couldnt decipher what to do with them.
![Screenshot (327)](https://user-images.githubusercontent.com/108130729/230703978-bced3438-e01b-4528-9865-93643e543167.png)

Finally, applying my knowledge of 'Fact' and 'Dimension' tables work in conventional 'star schema' and the ability to identify Primary keys and Foreign keys in these tables, I was able to connect data from one department to another department. For Instance, Most of the data in Human Resources department tables had connectors in the in most Sales table data because Sales teams includes employees who have records in the Human resources. Connecting them was seamless. There had to be connceting keys in these tables. 

In addition to that, the problem of cardinality, having to define what type of cardinality two tables connecting each other have. Normally, In a star schema, there ought to be mostly One-to-many relationships through out the schema but in the case of this project, I found out there was a mix of one-to-many and many-to-many relationships because there is data of 6 departments, each containing a number of tables to be inter-connected to each other.

Below is the resultant model having worked extensively on it.
Screenshot shows the all round Inter and Intra connectivity of all the tables, the final result of the modelling arranged according to departments;
![Screenshot (329)](https://user-images.githubusercontent.com/108130729/230706277-9073b193-241d-4208-aa8c-d5f58dbc6e5a.png)

Human Resources Department tables and how they connect to each other and beyond the department;
![Screenshot (330)](https://user-images.githubusercontent.com/108130729/230706304-b4556f3f-baf2-4ebb-8409-b48440344039.png)

Sales Department tables and how they connect to each other and beyond the department;
![Screenshot (333)](https://user-images.githubusercontent.com/108130729/230706333-c971b950-d540-4e7e-8422-fe2eba5976c3.png)

Purchasing Department tables and how they connect to each other and beyond the department;
![Screenshot (334)](https://user-images.githubusercontent.com/108130729/230706341-e7602579-e75c-4319-8703-1b052f1ca61f.png)

Person tables and how they connect to each other and beyond the department;
![Screenshot (336)](https://user-images.githubusercontent.com/108130729/230706367-a6882a58-2b62-488d-8d6a-c6e654fe6492.png)

Production Department tables and how they connect to each other and beyond the department;
![Screenshot (337)](https://user-images.githubusercontent.com/108130729/230706372-6354d135-df80-463d-82db-9a6ceb35486f.png)

# I Appreciate you taking time to give my documentation a read.

# You can connect with me on
https://twitter.com/KamalBI_ and ktaiwobiz@gmail.com

