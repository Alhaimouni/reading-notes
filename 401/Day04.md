# SQL database, ORM, Sequelize
#### What is SQL ?
<pre>Structured Query Language (SQL) is a standardized programming language that is used to manage relational databases
and perform various operations on the data in them. Initially created in the 1970s. </pre>

### SQL Command Types :
<ul>
  
<li>Data Definition Language (DDL) commands : are also called data definition commands because they are used to define data tables.</li>
<li>Data Manipulation Language (DML) commands : are used to manipulate data in existing tables by adding, changing or removing data. Unlike DDL commands that define how data is stored, DML commands operate in the tables defined with DDL commands.</li>
<li>Data Query Language : consists of just one command, SELECT, used to get specific data from tables. This command is sometimes grouped with the DML commands.</li>
<li>Data Control Language commands : are used to grant or revoke user access privileges.</li>
<li>Transaction Control Language commands : are used to change the state of some data -- for example, to COMMIT transaction changes or to ROLLBACK transaction changes.</li>
</ul>

### Differences between SQL and NoSQL :
![Diffrances between sql and nosql](https://cdn.ttgtmedia.com/rms/onlineimages/characterisitcs_of_relational_vs_nonrelational_databases-f.png)

### What is Sequlize ?
Sequelize is a modern TypeScript and Node.js ORM for Postgres, MySQL, MariaDB, SQLite and SQL Server, also
featuring solid transaction support, relations, eager and lazy loading, read replication and more.

### How to use it with Node js ?

   INSTALL DEPENDENCIES
   
    npm install sequelize sqlite3

DEFINE MODELS

    import { Sequelize, Model, DataTypes } from 'sequelize';

    const sequelize = new Sequelize('sqlite::memory:');
    const User = sequelize.define('User', {
      username: DataTypes.STRING,
      birthday: DataTypes.DATE,
    });

PERSIST AND QUERY

    const jane = await User.create({
      username: 'janedoe',
      birthday: new Date(1980, 6, 20),
    });

    const users = await User.findAll();

### What is an ORM, how does it work, and how should I use one?

<pre>Object-relational mapping (ORM) is a programming technique in which a metadata descriptor is used to connect object
code to a relational database.Object code is written in object-oriented programming (OOP) languages such as Java or C#.
ORM converts data between type systems that are unable to coexist within relational databases and OOP languages. </pre>

<pre>resolves the object code and relational database mismatch with three approaches: bottom up, top-down and meet in themiddle.
Each approach has its share of benefits and drawbacks. When selecting the best software solution,
developers must fully understand the environment and design requirements</pre>
