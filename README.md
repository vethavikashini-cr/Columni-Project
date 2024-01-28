# Columni
The project is a digital platform designed for Columbia University alumni, enabling them to create personal profiles, connect with fellow graduates, and engage in various community activities. This platform, tailored specifically for alumni, offers features like profile customization with educational and professional details, post creation for jobs, events, and social interactions, and a robust communication system for messaging other users. Additionally, a specialized admin role is designated for a limited number of users, primarily for content moderation and database management, ensuring a secure and dynamic online community for Columbia University's alumni network.


## Personas and Roles 
There are two personas:
### Alumni
A User is an alumni of Columbia University. Each user is associated with a schoolID which connects them to the school they attended at Columbia University. Users have the ability to create a profile with a Columbia email address, graduation year, and their major. They can optionally add their job title, company, profile picture, and user description. Users will be able to login using their Columbia email and password. Users are able to create posts of different types, such as job posts, event posts, and social posts. Users can comment on and like posts. Users can also send messages to other users.
### Admin
A User can be an administrator which allows privileges to delete any post, message, or profile incase of sensitive information or in case an update needs to be made to the database. There will only be 5 admin Users on our system, which is the 5 team members. This is mostly to provide more functionality to developers working on the GUI to easily make changes to the database. 

## Key Features: 
### A User can:
Create an account with a valid graduation date, Columbia email, major, and password.
Log in using their email and password.
Edit their profile, add a profile picture and bio.
Users can optionally add a job title and company.
Create posts that are categorized as social, job, or event posts.
Create comments and likes on posts.
Send messages to other Users.


### An Admin can:
Do everything a User can do with certain privileges such as: 
Delete any message, post, or profile in case of sensitive information.
Easily modify the database using the GUI.

## Domain Model Diagram

<img width="532" alt="image" src="https://github.com/vethavikashini-cr/Columni-Project/assets/145593646/8814d686-ab11-4b21-9cb7-d770ed3a90e1">

Firstly, there are Users, which have multiple fields. A user has an ID, a schoolID, an isAdmin flag, a first and last name, email, password, picture, major, job title, and description associated with their profile. These users are associated with messages and posts, in which the userID is used as a Foreign Key to link the tables together. Users are linked to messages, and messages are linked to threads. A user can have 0 to many messages, and a thread can have 1 to many messages. A user can have 1 or many schools associated with their account. A user can have 0 to many posts associated with their account, and a post can take on 4 forms, a comment, social, job, or event post. A post can have 0 to many likes as well.

## Logical View 
<img width="448" alt="image" src="https://github.com/vethavikashini-cr/Columni-Project/assets/145593646/d2d318f9-c547-467c-832c-2c4b65d7ccce">

## Physical View
<img width="485" alt="image" src="https://github.com/vethavikashini-cr/Columni-Project/assets/145593646/8bad10a7-0fad-4092-8948-e50a883e6e26">

## GCP Configuration:
App Engine: Deploy the posts microservice on GCP App Engine VMs, leveraging PaaS capabilities for easy management and deployment.
Cloud SQL: Use Cloud SQL as a responsive and interactive database service that integrates seamlessly with App Engine.
Services Under Consideration: Explore Compute Engine for its auto-scaling feature, which outperforms App Engine in dynamic load management, adapting to fluctuating traffic patterns efficiently.

## AWS Configuration:
Compute Service:Engage Amazon EC2 instances for the posts microservice, providing a diverse range of computing power options to match specific workload requirements.
Storage:Opt for Amazon S3 for its massive scalability as an object storage service, suitable for data storage needs, archiving, and backup strategies.

## Enhance Microservices Implementation

- [x] Core operations (GET, PUT, POST, DELETE) from each microservice.


## Events, Notifications, Pub/Sub

- [ ] Make a request to a microservice and Lambda function handling the published events.

## Composition/Aggregators

- [ ] Demonstrate a synchronous call that prints a log when getting a response from each microservice.
- [ ] Demonstrate an asynchronous call that prints a log when getting a response from each microservice. (repeat it 10 times, and it should microservices should be done in a different order at least once).

## API Gateway

- [ ] Demonstrate your API Gateway Implementation, which shows both authorized and unauthorized cases.

## Single Sign-On (SSO)

- [x] Demonstrate SSO login and make an authorized request using the given token.

## External API

- [ ] Explain what External API you are using and what this is for in your application, and demonstrate the functionality.

## Middleware

- [ ] Introduce one Middleware functionality in your application and explain what it does.

## CI/CD

- [ ] Demonstrate your CI/CD pipelines running on specific events.

## Infrastructure As Code

- [ ] Deploy and shut down any simple infrastructure in your project.

## GraphQL

- [x] Implement a simple example of GraphQL using one of the functionalities of your application.
