# Tech Quiz CI/CD Check Tests & Render Deployment
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

[Take the Python Tech Quiz!](https://ci-cd-testing-72de.onrender.com)

## Table of Contents

- [Description](#description)
- [Visuals](#visuals)
- [Installation](#installation)
- [Technologies Used](#technologies-used)
- [Key Features](#key-features)
- [Usage](#usage)
- [Support](#support)
- [Contributing](#contributing)
- [License](#license)

## Description

Tech Quiz is a web application that tests a users' knowledge of Python through a series of 10 randomly generated questions. Upon completion, the user is provided a score (#/10) and the option to re-take the quiz with potentially different questions, in a non-identical order. This app was built with Typescript, React and Node.js; also utilizing MongoDB for a scalable data/question management system.

This repo contains additonal code tailored to Github Actions workflow for the app. You can find the parent repo for Tech Quiz [here](https://github.com/iamthesaint/tech-quiz).
Specifically, this repo provides developers with automatically triggered Github Actions that ensure Cypress tests pass when pushing new code to the Develop branch, and when the passing code is merged into the Main branch, the Render web service will automatically redeploy with the updates.

## Visuals
*Deploy To Render Github Action*

<img width="2022" alt="Screenshot 2024-10-29 at 5 27 37 PM" src="https://github.com/user-attachments/assets/48fb6a99-734a-4950-9c24-f21482fca712">

*Checking Tests Github Action*

<img width="2022" alt="Screenshot 2024-10-29 at 5 28 20 PM" src="https://github.com/user-attachments/assets/b7de3903-2a81-4c69-9229-3342b2b78c8a">

## Installation

**Pre-reqs:** MongoDB installed locally with Mongoose, or an instance on MongoDB Atlas and Node.js packages. Cypress used for component and end-to-end testing, if testing is desired.
Github Actions YAML files used to provide TQ with branch protection.

## Technologies Used

- **Client-side:** React with Typescript and JSX Components
- **Server-side:** Node.js with Express, Typescript, and Mongoose
- **Database:** MongoDB for storing quiz question data
- **Testing:** Cypress for e2e and component testing
- **Branch Protection:** Github Actions

## Key Features

- **Randomized Questions:** Each quiz session generates a set of 10 questions in a different order.
- **Dynamic Question Flow:** Users are brought through the test questions quickly and smoothly without distraction.
- **Scoring:** Users receive a score out of 10 at the end of each quiz.
- **Retake Option:** Users can retake the quiz with a new set of questions.
- **Responsive Design:** The app is fully responsive and works on various devices via React.
- **User-Friendly Interface:** Simple and intuitive interface for seamless user experience.
- **Scalable Backend:** Utilizes MongoDB for efficient data management and scalability with a database that allows for flexible storage. MongoDB also provides an easy way for app-creators to continue adding questions as the application grows.
- **Comprehensive Testing:** Includes end-to-end and component testing with Cypress, ensuring the user journey is seamless and bug-free.

## Usage

- **Start the app:** 
```npm run start``` after seeding the database (```npm run seed```) with questions provided by the MongoDB collection.
- **Start the quiz:**
on the homepage of the app, you are greeted with a 'Start Quiz' button. Once clicked, the first question will be displayed.
- **Answer the questions:**
each question will take up an entire page with a list of possible answers. To select an answer, choose the blue number next to your answer. Once an option is selected, the next question will be displayed.
- **View your score:** 
when ten questions have been answered, your score -- the number of questions correct out of 10 -- will be visible.
- **Retake the quiz:**
if you are unhappy with your score, require more practice, or simply want to test your knowledge on another set of questions, choose the 'Retake Quiz' button and you will be presented with the first of a new set of questions.

## Support

For questions, comments, or a cup of coffee -- reach out to me at stephenie2@me.com, or my Github: [iamthesaint](https://github.com/iamthesaint)

## Contributing

If you wish to contribute to Tech Quiz, please fork the repo to create your additions/modifications. Keep in mind, you will require a .env file with the MONGODB_URI environment variable. In order to apply your changes to the deployed application, your code will need to pass the provided Cypress Tests, automatically triggered via pull-requests to Develop.

## License

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file in the repo for details.
