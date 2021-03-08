# E-commerce Back End &nbsp;&nbsp;&nbsp;[![MIT](https://img.shields.io/badge/license-MIT-yellow?style=for-the-badge)](https://shields.io/)

## Description

E-commerce back-end using MySQL. This express.js API forms the backend for an e-commerce website. Categories, Products, and Product Tags can be viewed, added, edited, and deleted from the database using a third-party API client such as Insomnia Core. 

![App screenshot](./assets/images/api-screenshot.png)

# Table of Contents
1. [Requirements](#requirements)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Questions](#questions)
5. [License](#license)

## Requirements
To use this app, you must have the following installed:
- [Node.js](https://nodejs.org/en/)
- [MySQL](https://dev.mysql.com/downloads/mysql/)
- [Insomnia Core](https://insomnia.rest/products/insomnia) or a similar API client.

A basic knowledge of the command line is also required. See [here](https://datacarpentry.org/shell-genomics/02-the-filesystem/index.html) for help navigating directories in the command line.

## Installation

1. To install the app, clone the respository above, or download as a .zip file.

![Image of download button](./assets/images/installation-1.png)

![Download options](./assets/images/installation-2.png)

2. In the command line, navigate to the directory containing the downloaded repsitory.
3. Download the required dependencies by typing the following in the command line: `npm install`

## Usage
To add your MySQL credentials:
1. In the root directory of the app, create a file called `.env`
2. Open the `.env` file, and enter the database name ('ecommerce_db'), and your MySQL credentials in the following format: 

```
DB_NAME='ecommerce_db'
DB_USER='root'
DB_PW='password123'
```

To create the database:
1. Enter the MySQL CLI by entering `mysql -u root -p` followed by your MySQL password.
2. Create the database by entering `source db/schema.sql`.
3. Return to the command line by entering `quit`.
4. Seed the database by entering `npm run seed` in the command line (not the MySQL CLI).

To make requests to the database:
1. In the root directory of the app, start the server by entering `npm start` in the command line.
2. Enter the URL `http://localhost:3001/api` in Insomnia Core.
3. In Insomnia Core, you can make GET, POST, PUT, and DELETE requests for categories, products, and product tags to update the database.

A video walkthrough of the API requests being tested in Insomnia Core can be found [here](https://drive.google.com/file/d/1f4tVzQpUijBDjdZnTxcCW1WMFDQNAxcE/view?usp=sharing).

## Questions
For additional questions, contact Amelia:

GitHub: [amelia-was](https://github.com/amelia-was)

## Built Using
- JavaScript
- Node.js
- Express.js
- MySQL with the MySQL2 and Sequelize packages for node.js

## License
Under the MIT license, this material is free to modify and distribute for commercial or private use. See [here](https://opensource.org/licenses/MIT) for more details.
