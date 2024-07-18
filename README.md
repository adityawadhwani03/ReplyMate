ReplyMate

Description: ReplyMate is a Node.js application that automates the process of responding to unreplied emails during a specified period, such as a vacation. It leverages the Gmail API to interact with your Gmail account and perform actions like sending automated replies and labeling emails related to your vacation.

Table of Contents
1. Features
2. Getting Started
3. Prerequisites
4. Installation
5. Obtaining Credentials
6. Configuration
7. Usage

Features
- Automatically sends a predefined vacation response to emails that haven't been replied to.
- Labels incoming emails during your vacation period for better organization.
- Periodically checks for unreplied emails and responds accordingly.



Getting Started

Prerequisites
- Node.js installed on your machine. You can download it [here](https://nodejs.org/).
- Gmail API credentials:
  - Follow the instructions in the "Obtaining Credentials" section to create a project, enable the Gmail API, and obtain the credentials.json file.

Installation
1. Clone the repository
 
2. Navigate to the application folder:

3. Open the codebase in your IDE:
   code .
   

4. Install the dependencies:
   npm install
   

5. Run the application:
   node index.js
   

   The application will start on http://localhost:5000.

Obtaining Credentials
To use the Gmail API, set up API credentials by following these steps:

1. Visit the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project.
3. Enable the Gmail API for your project.
4. Configure the OAuth consent screen.
5. Set the necessary scopes:
    - https://www.googleapis.com/auth/gmail.readonly
    - https://www.googleapis.com/auth/gmail.send
    - https://www.googleapis.com/auth/gmail.labels
    - https://mail.google.com/
6. Download the credentials file and rename it to credentials.json.
7. Place the credentials.json file in the root directory of the ReplyMate application.

Configuration

1. Set the labelName variable in index.js to define the label for vacation-related emails.
2. Customize the vacation response message in the sendReply function.
3. Adjust the interval for checking emails, which is randomly set between 45 to 120 seconds, in the setInterval function.

Usage

1. Access the application by visiting http://localhost:5000 in your browser.
2. Authenticate with your Gmail account using the credentials in credentials.json.
3. Once authenticated, the application will create a label for vacation-related emails (if it doesn't already exist) and periodically check for unreplied emails, sending automated responses and applying the vacation label as needed.
