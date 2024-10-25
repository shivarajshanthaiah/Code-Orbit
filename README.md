# Code Orbit
Code Orbit is a web-based platform for code challenges with features like code submission, chat, and admin tools to manage users, problems, and test cases. 
Built with Golang microservices using gRPC, it leverages PostgreSQL, MongoDB, Redis, and RabbitMQ for seamless performance. 
Users benefit from OTP-based authentication via Twilio, Razorpay-powered subscriptions, real-time rankings, and automated email notifications. 
The platform provides a smooth programming experience with advanced error handling and exclusive perks for prime members.

## Live Demo
To access the live demo of this project, please visit my API documentation and test it using any API testing software.
Detailed API documentation link - https://documenter.getpostman.com/view/32823353/2sAY4siPR5

## Features

- Added SMS OTP verification for enhanced user security.
- Supports code submissions in Golang.
  - Handles typos, syntax errors, and compilation errors.
  - Displays results based on test cases passed.
  - Users can view their rankings.
- Generates invoices after successful subscription selection.
- Invoices are sent via email.
- Admin Panel: Provides full control over the system.
- Admin can add problems and test cases with edge cases.
- Chat Feature: Users can communicate with each other.
- Prime Membership: Offers exclusive benefits for subscribers.

### User Features

- **Authentication:**
  - User registration with SMS OTP verification.
  - Login with credentials.
  - JWT authentication

- **Submission Management:**
  - View submission history and problem details.
  - Get feedback for submitted code.
  - Proper error handling.

### Admin Features

- **User and Role Management:**
  - Manage Users.
  - Manage Problems, Testcases.
  - Dashboard with access to every ongoing information.

## Technologies Used

- **Backend:**
  - Go language.
  - Gin web framework
  - gRPC for inter-service communication.
  - PostgreSQL for data storage.
  - MongoDB for schemaless data storing.
  - Redis for caching.
  - Twilio for SMS OTP verification.
  - Razorpay for payment processing.
  - RabbitMQ for message queuing.
  - SMTP for email notifications.
  - GORM as the ORM.

- **Containerization:**
   - Docker
   - Kubernetes

## Setup and Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/Code-Orbit.git

2.Install dependencies:

    cd code-orbit
    go get -u github.com/gin-gonic/gin
    go get -u google.golang.org/grpc/
    go get -u github.com/razorpay/razorpay-go
    go get -u github.com/go-redis/redis
    go get -u gorm.io/driver/postgres
    go get -u github.com/twilio/twilio-go

3.Set up the database:

    CREATE DATABASE codeorbit
    install the UUID extension
    

4.Configure environment variables:

    GRPCADMINPORT:    #########
    GRPCUSERPORT:     #########
    GRPCPROBLEMPORT:  #########
    GRPCCHATPORT:     #########

    DB_Config="host=localhost user=##### password=***** dbname=******* port=0000 sslmode=disable"  
    MONGODB_URL = mongodb+srv:##########:neo6lQjerEyggJky@#######.xdo0n.mongodb.net/********?retryWrites=true&w=majority&appName=########
    MONGODB_NAME = *******

    rabbitMQ="amqp://guest:guest@localhost:5672/"


    Email="youremail@email.com"
    Password="__ __ __ __(use app password)"
    
    
    RAZORPAY_KEY_ID="________________(apikey)"
    RAZORPAY_SECRET="_______________(api secret)"


    TWILIO_ACCOUNT_SID="___________________"
    TWILIO_AUTHTOKEN="_____________________"
    TWILIO_SERVIES_ID="___________________"
    TWILIO_PHONENUMBER="__________________(twilio phone number)"

5.Run the application:

    make run

### If you wish to run docker Image clone docker compose file
    Docker-compose up
       
