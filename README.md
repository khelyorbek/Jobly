## **Jobly**
### All the jobs in one, convenient place.

---
## **How to run the application?**
### **Method 1: Running the application online**
[**CLICK HERE TO OPEN THE APPLICATION ONLINE**](https://jobly.elyorbek.com/) 
- or copy-paste https://jobly.elyorbek.com/ into your browser
- If you need to interact with the backend, the endpoint is: https://jobly-backend.elyorbek.com/


### **Method 2: Running the application locally**
1. Download this repository to your local computer
2. Make sure you have `npm` installed or check [this page](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) on how install it
3. Make sure you have `psql` (PostgreSQL) installed or check [this page](https://www.postgresql.org/download/) on how to install it
4. Open command prompt on your computer
5. In your command prompt, navigate to the folder where you have this repository
6. Go into backend folder and run `npm install` to install dependencies
7. Go into frontend folder and run `npm install` to install dependencies (Note: this might take a while)
8. Load the sample data into a PostreSQL database
    1. Start your PostgreSQL server by typing `sudo service postgresql start`
    2. Type `psql` to open PostgreSQL
    3. Run the sql file by typing `\i backend/jobly.sql`
    4. Wait for the import to complete and accept any message that come up
    5. Exit psql by typing `\q`
    6. Open the backend folder
    7. Open the file called config.js
    8. Replace this string with your PostgreSQL configuration `postgresql://test:test@localhost/jobly`
        - The format above is `postgresql://username:password@localhost/databasename`
        - username = your PostgreSQL account username that you configured on install
        - password = your PostgreSQL account password that you configured on install
        - localhost = address to your PostgreSQL server. Usually just localhost
        - databasename = is the name of the database. In our case its jobly
    9. Save the config.js file
9. Go back to the root of the repository folder
10. Go into backend folder and run `npm start` to start the backend Express server
11. Go into frontend folder and run `npm start` to start React application (Note: this might take a while)
12. The address `https://localhost:3000` should open automatically but if it doesn't, go to that address in any browser (I recommend Chrome)
13. Have fun!

---

## React Component Design Schema
![React component design](/screenshots/react_components.png)

---

## Screenshots of the application
![Main page](/screenshots/1.png)

![Login page](/screenshots/2.png)

![Sign up page](/screenshots/3.png)

![Home page](/screenshots/4.png)

![Company list page](/screenshots/5.png)

![Company details page](/screenshots/6.png)

![Jobs page](/screenshots/7.png)

![Jobs page](/screenshots/8.png)

![Profile page](/screenshots/9.png)

![Profile page](/screenshots/10.png)

