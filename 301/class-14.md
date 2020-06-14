# Normalization
1. Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included. Take a spreadsheet containing the information as an example, where the data contains salespeople and customers serving several purposes:

  > Identify salespeople in your organization
  > List all customers your company calls upon to sell a product
  > Identify which salespeople call on specific customers.
1. There are three main reasons to normalize a database.  The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries. 
1. Duplicated information presents two problems:
  > It increases storage and decrease performance.
  > It becomes more difficult to maintain data changes.
1. Insert Anomaly - There are facts we cannot record until we know information for the entire row
1. Update anomaly - In this case we have the same information in several rows
1. Deletion Anomaly - Deletion of a row causes removal of more than one set of facts.
1. Definition of Database normalization - There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively.
1. First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
1. Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
1. Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key

# Project Ideas - 
1. I still think it would be fun to have an app called weekend warrior.  WE could use the Trails API from the labs, and geodata.  