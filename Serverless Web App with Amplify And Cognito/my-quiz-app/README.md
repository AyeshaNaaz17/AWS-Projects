# React App with AWS Amplify, Cognito, and CI/CD

## Overview

This project demonstrates how to build a React application with authentication using AWS Amplify and Amazon Cognito. It also covers the CI/CD process by hosting the application on AWS Amplify and integrating it with GitHub for continuous deployment.

### Features
- **React App**: Frontend built using React.
- **Authentication**: Secure user authentication managed by Amazon Cognito.
- **Continuous Deployment**: Automated CI/CD pipeline using AWS Amplify and GitHub.

## Prerequisites

Before you begin, ensure you have the following:
- AWS Account with admin access.
- Node.js and npm installed on your local machine.
- Git installed on your local machine.
- A GitHub account.

## Project Setup

### 1. Set Up Environment

1. Create a new folder for your project and navigate into it using the terminal:
   ```bash
   mkdir my-react-app
   cd my-react-app
2. Install the AWS Amplify CLI globally:
   ```bash
   npm install -g @aws-amplify/cli

  ![Screenshot 2024-08-11 105327](https://github.com/user-attachments/assets/683d0b77-106d-4923-8e5d-c52bc5b5db4b)

   
3. Configure the Amplify CLI to work with your AWS account:
   ```bash
   amplify configure
  a) Sign in to your AWS account with admin access.
  b) Select your preferred AWS region.
  c) Create a new IAM user specifically for this project.

  ![Screenshot 2024-08-11 105715](https://github.com/user-attachments/assets/220d9eaa-b043-4754-bd07-e0aaa23436b9)
  
  ![Screenshot 2024-08-11 105749](https://github.com/user-attachments/assets/28e9421d-1944-44cd-b512-68fbd6d43640)

  ![Screenshot 2024-08-11 105834](https://github.com/user-attachments/assets/00113c21-edb7-411d-b20c-69a07926c06a)

  ![Screenshot 2024-08-11 105924](https://github.com/user-attachments/assets/204801e9-3b04-42c5-9aaf-34edc440fcc4)

  ![Screenshot 2024-08-11 105937](https://github.com/user-attachments/assets/bce306d5-1b78-495b-a76a-de18a98de652)

  ![Screenshot 2024-08-11 105952](https://github.com/user-attachments/assets/e9270e62-cb0c-4878-8081-d641709c28a2)

  ![Screenshot 2024-08-11 110003](https://github.com/user-attachments/assets/11106a05-567e-48b2-b9bf-2213ff4b44db)

  ![Screenshot 2024-08-11 110028](https://github.com/user-attachments/assets/22f4e08e-3907-41fa-bd4d-9c5cf4f86fc5)

  ![Screenshot 2024-08-11 110117](https://github.com/user-attachments/assets/906f5f12-4cf8-4cd0-8c6d-297a0c97fe24)


  d) Enter the IAM user's access key and secret access key.

   ![Screenshot 2024-08-11 110142](https://github.com/user-attachments/assets/9aca1c09-7c28-4328-a514-d29245cc419e)

   ![Screenshot 2024-08-11 110224](https://github.com/user-attachments/assets/da0f377d-56bf-4ae2-a210-b04f3dfcbdde)

    
  e) Provide a profile name for the configuration.

   ![Screenshot 2024-08-11 110308](https://github.com/user-attachments/assets/7b9fe8b4-785d-4370-b2aa-0ca1d76e2791)


### 2. Create a React App

1. Create a new React application:
   ```bash
   npx create-react-app my-app
2. Navigate into the project directory:
   ```bash
   cd my-app
3. Initialize an Amplify project within the React app:
   ```bash
   amplify init

  ![Screenshot 2024-08-11 110941](https://github.com/user-attachments/assets/0a6b5ba7-dc87-43d9-948c-9968223a7bb7)

  a) Enter the project name.
  b) Select the AWS profile created earlier.

  ![Screenshot 2024-08-11 110941](https://github.com/user-attachments/assets/c1483c3a-eed9-4beb-b4e2-76cba8c2ad4f)


### 3. Add Authentication with Amazon Cognito

1. Add authentication to your app using Amplify:
   ```bash
   amplify add auth
  Follow the prompts to configure authentication settings.

  ![Screenshot 2024-08-11 112050](https://github.com/user-attachments/assets/5686e6ed-1083-4119-8870-d3c586c74b86)

  
2. Push the changes to the cloud:
     
    amplify push

   ![Screenshot 2024-08-11 112736](https://github.com/user-attachments/assets/9c51fce0-731c-4c29-97e8-e90028542a70)


### 4. Add Functionality to the Project

1. Install necessary Amplify libraries for React UI:
   ```bash
     npm install aws-amplify @aws-amplify/ui-react

2. Modify the React code to include authentication features.
   
3. Run the application locally to test the authentication:
    ```npm start```

     a) Access the app on http://localhost:3000.
   
     b) Test account creation and login. Verify that users are being created in the Cognito User Pool.

      ![Screenshot 2024-08-11 113935](https://github.com/user-attachments/assets/7bdd61d7-32c2-4a7f-964c-36e827f8df82)

      ![Screenshot 2024-08-11 112913](https://github.com/user-attachments/assets/274b4a84-2090-4f55-afef-8c66a5e3a796)




### 5. Push Local Code to GitHub

a) Initialize a Git repository in your project: ```git init```
b) Add and commit your changes:
      ```git add .
      git commit -m "Initial commit"```
c) Create a new private repository on GitHub.
d) Push your code to GitHub:

    git branch -M main
    git remote add origin https://github.com/your-username/your-repo-name.git
    git push -u origin main

### 6. Hosting and CI/CD with AWS Amplify

1. In the AWS Console, navigate to Amplify -> All apps -> Select your app.
2. Deploy your app using GitHub as the source:
    a) Update GitHub permissions to select the correct repository.
    b) Select the backend environment and create a role with Amplify admin access.
    c) Save and deploy.

  ![Screenshot 2024-08-11 114937](https://github.com/user-attachments/assets/e2eb0839-25f1-4e40-ad55-751a70e52594)

  ![Screenshot 2024-08-11 114959](https://github.com/user-attachments/assets/0d710477-6361-4763-b757-708129884e83)

  ![Screenshot 2024-08-11 115053](https://github.com/user-attachments/assets/d5211ba1-fd4e-4d63-9eda-d03e9d89f63d)

  ![Screenshot 2024-08-11 115320](https://github.com/user-attachments/assets/6e0fc17e-6ada-4358-b131-c219741ba794)

  ![Screenshot 2024-08-11 115515](https://github.com/user-attachments/assets/12562321-e93e-4d4f-aa72-178bbf700a49)

  ![Screenshot 2024-08-11 115515](https://github.com/user-attachments/assets/9656ff90-46e3-4a90-9225-6046ceeaec3e)

  ![Screenshot 2024-08-11 115805](https://github.com/user-attachments/assets/517649ee-9aa5-4bc8-826a-60a03387dce0)

  ![Screenshot 2024-08-11 115816](https://github.com/user-attachments/assets/da0e404d-41ba-4b22-b5fa-b5a459e3d344)

  ![Screenshot 2024-08-11 115830](https://github.com/user-attachments/assets/9bb8800f-dd79-4672-b04e-b063cb8c86b1)

  ![Screenshot 2024-08-11 115830](https://github.com/user-attachments/assets/53c3d2d2-f20c-4696-b920-52256ac6ad91)

  ![Screenshot 2024-08-11 115951](https://github.com/user-attachments/assets/2fb399d9-3e7d-46cd-859d-c1bb171cb920)

  ![Screenshot 2024-08-11 120241](https://github.com/user-attachments/assets/13ca1d9b-66f3-44fe-833a-6217820c671b)

   
4. Access the deployment link provided by Amplify to view your live application.

  ![Screenshot 2024-08-11 120719](https://github.com/user-attachments/assets/cd1a08da-1305-4f11-9cbc-cc32ab8096da)

  ![Screenshot 2024-08-11 120800](https://github.com/user-attachments/assets/7edf6648-f5bb-49a7-80bf-649849cb4ec1)


### 7. Testing CI/CD

1. Make changes to any file in your GitHub repository (e.g., update a quiz question).
2. Push the changes to GitHub.
3. Amplify will automatically detect the changes and trigger a new build and deployment.

   ![Screenshot 2024-08-11 121323](https://github.com/user-attachments/assets/e64f7e92-d032-4a5f-a7ed-1445149c4131)

   ![Screenshot 2024-08-11 120934](https://github.com/user-attachments/assets/58fb7d30-ebc5-4786-b680-f9f6f8e5b90e)

   ![Screenshot 2024-08-11 120945](https://github.com/user-attachments/assets/1b038999-2841-4753-aee7-2d233c937f98)

   ![Screenshot 2024-08-11 121002](https://github.com/user-attachments/assets/94947823-c8f9-4e31-bd51-e12d6cd53841)

   ![Screenshot 2024-08-11 121313](https://github.com/user-attachments/assets/e30b7ed7-4d97-4bd5-b358-7f4ae629dc21)


### 8. Clean Up

Don't forget to delete the AWS resources created to avoid unnecessary charges.

  - Delete your amplify app from the aws console 
    ![Screenshot 2024-08-11 131759](https://github.com/user-attachments/assets/1426b029-8a66-4afd-81c8-33d662af5fcc)
  - Double check if the user role is created in cognito is deleted
  - Delete the role created for this project
  - Delete the IAM User created for this project (Optional)
