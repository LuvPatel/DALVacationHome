


# DALVacationHome

[](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#dalvacationhome)

DALVacationHome is a serverless, multi-cloud application designed for booking hotel rooms, offering users the ability to make reservations while allowing property agents to add, modify, and manage room listings. The platform includes a virtual assistant to respond to user inquiries and features a messaging system for communication between authorized users and agents.

## Table of Contents

[](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#table-of-contents)

-   [Features](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#features)
-   [Architecture](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#architecture)
-   [Modules](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#modules)
-   [Technologies Used](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#technologies-used)
-   [Setup Instructions](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#setup-instructions)
-   [Usage](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#usage)
-   [Testing](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#testing)
-   [Contributing](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#contributing)
-   [License](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#license)


## Features

-   **Guest Users:** Explore available rooms, check tariffs, and use a virtual assistant for basic navigation and feedback.
-   **Registered Customers:** Benefit from multi-factor authentication, book rooms, receive virtual assistant support, and submit feedback.
-   **Property Agents:** Access admin features to manage room listings, update details, and communicate with customers through the messaging system.

## Architecture

The application is deployed using a multi-cloud model, leveraging a mix of AWS and GCP services. It is designed on a serverless architecture, providing scalability and efficiency.

## Modules

1.  **User Management & Authentication**
    
    -   **Registration:** Implemented with AWS Cognito, DynamoDB, and AWS Lambda.
    -   **Multi-Factor Authentication:** Utilizes passwords, security questions, and Caesar cipher validation.
2.  **Virtual Assistant**
    
    -   **Bot Integration:** Built with Google Dialogflow, DynamoDB, and AWS Lambda.
    -   **Functionality:** Provides navigation assistance, room details retrieval, and facilitates customer-agent communication.
3.  **Message Passing**
    
    -   **Pub/Sub Messaging:** GCP Pub/Sub handles message exchange between customers and property agents.
    -   **Logging:** Communication logs are stored in DynamoDB.
4.  **Notifications**
    
    -   **Email Notifications:** AWS SNS and SQS manage notifications for registration, login, and booking confirmations.
    -   **Queue Processing:** SQS-triggered Lambda functions handle room booking approvals.
5.  **Data Analysis & Visualization**
    
    -   **Analytics Dashboard:** LookerStudio dashboard is embedded in the frontend for property agents.
    -   **Feedback Sentiment Analysis:** Customer feedback is analyzed using the Google Natural Language API.
6.  **Web Application & Deployment**
    
    -   **Frontend:** React-based application hosted on GCP CloudRun.
    -   **Deployment Automation:** Managed with CloudFormation.

## Technologies Used

[](https://github.com/jeffrypaul37/DALVacationHome?tab=readme-ov-file#technologies-used)

-   **Frontend**: React.js, Kommunicate.io
-   **Backend**: AWS Lambda, AWS Cognito, GCP Pub/Sub, GCP CloudRun, AWS Lex, API Gateway
-   **Database**: DynamoDB
-   **Analytics**: Google Natural Language API, LookerStudio
-   **Messaging**: GCP Pub/Sub, AWS SQS
-   **Notifications**: AWS SNS, AWS Cognito

## Setup Instructions

[](https://github.com/jeffrypaul37/DALVacationHome?tab=readme-ov-file#setup-instructions)

## Prerequisites

[](https://github.com/jeffrypaul37/DALVacationHome?tab=readme-ov-file#prerequisites)

-   Node.js and npm
-   Access to AWS and GCP services

## Installation

[](https://github.com/jeffrypaul37/DALVacationHome?tab=readme-ov-file#installation)

1.   Clone the repository
   ``` 
    git clone https://github.com/your-username/DALVacationHome.git
```    
2. Navigate to the project directory:
```
 cd DALVacationHome
```
3. Install dependencies:
```
 npm install
```
4. Set up environment variables for AWS and GCP services.
5.  Deploy the backend services using CloudFormation or GCP Deployment Manager.
6.  Start the development server:
  ```
     npm start
   ```

## Usage

[](https://github.com/jeffrypaul37/DALVacationHome?tab=readme-ov-file#usage)

-   Visit your deployed application at your CloudRun URL.
-   Guest users can browse rooms and interact with the virtual assistant.
-   Registered customers can log in, book rooms, and communicate with agents.
-   Property agents can manage properties and respond to customer queries.

## License

[](https://github.com/LuvPatel/DALVacationHome?tab=readme-ov-file#license)

This project is licensed under the MIT License.
