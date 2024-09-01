
**IMPORTANT:** All rights to this project, including its ideas and implementation, are copyright to Abhishek Gupta. Any use of this project or its ideas without explicit permission from the Abhishek Gupta is strictly prohibited and may result in serious consequences.

# Indian Sign Language - Text to Sign Animation

The **Indian Sign Language - Text to Sign Animation** project is a tool for converting text into sign language animations. Built with **Node.js, MongoDB, HTML, CSS, and JavaScript**, this application enables users to sign up, log in, convert text to sign language animations, upload new sign videos, and view their upload history.

## Demo Video

Watch the demo video to get a quick overview of how the application works:

https://github.com/user-attachments/assets/01f3cb8c-8a47-4422-a084-a8eabe6e63d0

---

## Table of Contents

- [Project Description](#project-description)
- [Features](#features)
  - [Signup](#signup)
  - [Login](#login)
  - [Landing Page](#landing-page)
  - [Home Page](#home-page)
  - [Upload](#upload)
  - [History](#history)
- [Setup and Installation](#setup-and-installation)
- [Running the Project](#running-the-project)
- [Contributing](#contributing)
- [License](#license)

## Project Description

This project provides a user-friendly interface for converting text into sign language animations. Users can sign up, log in, interact with a text-to-sign feature, upload new sign videos, and manage their uploaded content. MongoDB is used to store user and content data.

---

## Features

### Landing Page

- **Functionality:** The landing page provides a "Get Started" button to begin using the application.

- **Landing Page Image:**

  ![firstpage](https://github.com/user-attachments/assets/7025373d-ac96-4ba8-9336-31c48a360a87)

---

### Signup

- **Functionality:** Users can sign up by providing a username, email, and password. Duplicate users are alerted if an account already exists.

- **Sign Up Image:**

  ![signup](https://github.com/user-attachments/assets/bc0e3d31-d976-4a57-91b7-1f5c6b48c09f)

- **Duplicate User Alert:**

  ![duplicate](https://github.com/user-attachments/assets/5844ffc7-692f-49a5-9cb0-10a9c6182493)

---

### Login

- **Functionality:** Users can log in using their username or email and password. Password reset is supported. Login options are available through Google, Facebook, GitHub, and LinkedIn.

- **Login Image:**

  ![login](https://github.com/user-attachments/assets/d93ee72a-769c-4fe0-b389-cf4f3d180c58)

- **Wrong Password/Username Alert:**

  ![wrongpassword](https://github.com/user-attachments/assets/d56cc3ac-2986-432f-8f15-4e6fd3e29955)

---


### Home Page

- **Functionality:** The home page features a navbar with options for Home, Upload New Video, History, About, and Logout. Users can input text or use start record to speak and record text and then onvert to sign language animations. The entered text is displayed with highlighted words corresponding to the sign animation.

- **Home Page Image:**

  ![home-page](https://github.com/user-attachments/assets/c173e780-f545-4a1f-914e-56a9f90983c1)

---

### Upload

- **Functionality:** Users can contribute by uploading sign language videos with titles and descriptions. Videos are stored in the content collection in MongoDB. Admins review and authorize or remove the uploaded content.

- **Upload Image:**

  ![upload-video](https://github.com/user-attachments/assets/779ed1ea-fb86-4c5f-8ebc-05e491b0e394)

- **Upload Success/Failure Alert:**

  ![upload-success](https://github.com/user-attachments/assets/0e85e15b-2d84-46e0-9124-c86993fd3aee)

---

### History

- **Functionality:** This page displays a table of all videos uploaded by the user, including the video title, description, and upload date.

- **History Image:**

  ![history](https://github.com/user-attachments/assets/bc6b5c4f-ecc2-402b-9dfb-e4ed9597368f)

---
## Database Details

The application uses MongoDB for data storage. It has two main collections:

1. **Users Collection**
   - Stores user details such as:
     - `UserName`: The user's full name
     - `email`: User's email address
     - `password`: Hashed password
     - Security details such as salt for password hashing are also stored.

   ![mongodb collections](https://github.com/user-attachments/assets/0846c436-4ce1-4ce4-9e2e-b9e39fa5916f)

2. **Contents Collection**
   - Stores user-submitted sign video:
     - `userID`:    Id of the user
     - `updatedAt`: Timestamp when the user details were last updated
     - `VideoName`: User's first name
     - `VideoPath`: User's last name
     - `createdAt`: Timestamp when the user was created
     - `updatedAt`: Timestamp when the user details were last updated

   ![mongodb collections](https://github.com/user-attachments/assets/0846c436-4ce1-4ce4-9e2e-b9e39fa5916f)
   

## Setup and Installation

### Prerequisites

Before setting up the project, ensure you have the following installed:
- **Node.js** (Latest version)
- **MongoDB** (Local or remote instance)
- **NPM** (Node Package Manager)
- **A code editor** (e.g., Visual Studio Code)
- **A modern browser** (e.g., Chrome, Firefox)

### Installation Guide

1. **Clone the Repository**
   - Clone the project repository to your local machine:
     ```bash
     git clone https://github.com/KunvarAbhishek/SignLangauge-Text-To-Animation.git
     cd SignLangauge-Text-To-Animation
     ```

2. **Install Dependencies**
   - Navigate to the project directory using the terminal or command prompt:
     ```bash
     cd path_to_project
     ```
   - Install the required dependencies listed in the `package.json` file:
     ```bash
     npm install
     ```

3. **Set Up Environment Variables**
   - Look for a `.env.example` file in the project folder. If it exists, copy it to create a `.env` file:
     ```bash
     cp .env.example .env
     ```
   - Fill in the values in the `.env` file, such as the MongoDB connection string and any other required environment variables.

4. **Set Up MongoDB**
   - Ensure MongoDB is running. If you are using a local MongoDB instance, start the MongoDB service:
     ```bash
     mongosh
     ```

5. **Run the Project**
   - Start the Node.js application using one of the following commands:
     ```bash
     npm start
     ```
     or
     ```bash
     node index.js
     ```
      or
     ```bash
     npm i nodemon
     npm run dev
     ```


6. **Access the Application**
   - Once the application is running, open your browser and go to the URL specified in the project, typically:
     ```bash
     http://localhost:3000
     ```
     (Replace `3000` with the correct port if different.)



## Conclusion

The primary purpose of this project is to facilitate better communication for those who rely on sign language. By integrating modern technologies such as speech recognition and video processing, the application aims to provide a seamless experience for users to manage and view sign language content effectively.
