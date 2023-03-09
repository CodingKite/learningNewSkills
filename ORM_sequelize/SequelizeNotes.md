## What is Sequelize
- **Sequelize is a promise-based Node.js ORM tool** for relational databases like Postgres, MySQL, MariaDB, SQLite, Microsoft SQL Server, Oracle Database, Amazon Redshift and Snowflake’s Data Cloud.
- Object Relational Mapping(ORM) is an
  : technique of accessing(performing operations) a relational database from an Object oriented language.
  : technique that maps software objects with database tables.

- explain sequelize.authenticate()
  - sequelize.authenticate() is a method in the Sequelize library that is used to establish a connection with a SQL database.
  - When you call this method on a Sequelize instance, it sends a test query to the database to check if the connection is successful. If the connection is successful, the method returns a promise that resolves to true. If the connection fails, the method throws an error.
  - Note that sequelize.authenticate() does not actually create a new database or table if they do not exist. It only tests the connection to the existing database.
  - "Test the connection by trying to authenticate"
  - **You can use the .authenticate() function to test if the connection is OK:**
  - Here is an example of how sequelize.authenticate() can be used to connect to a MySQL database:

```js
const { Sequelize } = require('sequelize');

const sequelize = new Sequelize('database', 'username', 'password', {
  dialect: 'mysql'
});


sequelize.authenticate()
  .then(() => {
    console.log('Connection has been established successfully.');
  })
  .catch((error) => {
    console.error('Unable to connect to the database:', error);
  });

```

- what is Semantic Versioning??
  - Semantic Versioning, often abbreviated as SemVer, is a versioning system used for software development that provides a standardized way of managing and releasing version updates.
  - The SemVer system is based on a three-part version number: MAJOR.MINOR.PATCH.
    - The MAJOR version number indicates significant changes that are not backward compatible
    - the MINOR version number indicates added functionality in a backward-compatible manner,a
    - and the PATCH version number indicates bug fixes or minor changes that are backward compatible.
  - For example, if a software product has a version number of 1.2.3,
    - the 1 indicates the major version, 2 indicates the minor version, and 3 indicates the patch version.
    - If a change is made to the software that breaks backward compatibility, the major version should be incremented.
    - If new functionality is added in a backward-compatible manner, the minor version should be incremented.
    - If only bug fixes are made, the patch version should be incremented.
  - Semantic Versioning is widely used in the software development community as it helps to provide clarity and consistency when managing and releasing software updates, and helps ensure that different software components can work together effectively.

