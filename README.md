# Hospital API

A Server-side API built on NodeJS and MongoDB for hospital doctors to keep track of their patients with Covid19 test reports.
It is built using **MongoDB, ExpressJs, NodeJS and JavaScript.**

Hosted Link: [Hospital API](https://hospital-api-58bj.onrender.com)

# Functionality

* There can be 2 types of Users
    - Doctors
    - Patients
- Doctors can log in
* Each time a patient visits, the doctor will follow 2 steps
    - Register the patient in the app (using phone number, if the patient already exists, just
      return the patient info in the API)
    - After the checkup, create a Report
* Patient Report will have the following fields
    - Created by doctor
    - Status:
      - Can be either of: [Negative, Travelled-Quarantine, Symptoms-Quarantine,
        Positive-Admit]
    - Date

## Getting Started
* Fork the project
* Clone the forked repository in your local system
* Create .env file in the root directory and add the following:-
    - PORT="Your port number"
    - MONGODB_URL="Your MongoDB URL"
    - SESSION_SECRET_KEY="Your secret session key"
* Install all required packages
```bash
npm install 
```
* Run project 
```bash
npm start
```
The project is running on the port number provided by you.

# Routes in Hospital-API

* /doctors/register → with phone and password
* /doctors/login → returns the JWT to be used
* /patients/register
* /patients/:id/create_report → Create patients report
* /patients/:id/all_reports → List all the reports of a patient oldest to latest
* /reports/:status → List all the reports of all the patients filtered by a specific status

## Tools Used 
- NodeJS
- MongoDB
- ExpressJS

### Libraries: 
* dotenv
* express
* express-session
* jsonwebtoken
* nodemon
* mongoose
* passport
* passport-jwt
* mongodb
* bcryptjs