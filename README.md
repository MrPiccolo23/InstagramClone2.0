


# InstagramClone-2.0

## Description

This is an Instagram 2.0 clone web application built with REACT.JS! (Next.js, Tailwind CSS, Firebase v9, NextAuth, Recoil).

## Setup Instructions

### Prerequisites

- Node.js
- npm or yarn
- Firebase account

### Firebase Setup

1. Create a new Firebase account or log in to your existing account.
2. Click on the "Get started" button.
3. Click on "Add project" or "Create project".
4. Name the project (for instance, "insta-app") and click "Continue".
5. Do not enable Google Analytics for this project.
6. Click "Create Project" and wait for the project to be initialized.
7. Navigate to the "Authentication" section and click "Get started".
8. Enable "Email/Password" and "Google" as sign-in methods. For Google sign-in, select "project-supported email" and choose your default Google email.
9. Navigate to the "Storage" section and click "Get started". Start in test mode since this project is only a demo. Click "Next".
10. Choose a Cloud Storage location that's nearest to you (for instance, "nam5 (us-central)" for USA or "eur3 (Europe-west)" for Western Europe). Once you've selected your server, click "Done".
11. Go back to the project overview and add the "Cloud Firestore" database. You don't need to configure this in the Firebase console as it will be accessed via the `getFirestore` import from "@firebase/firestore" in the code.
12. Finally, go to the project settings (click on the gear icon, then "Project Settings").
13. Click on the "</>" icon to add a web app. Give the app a nickname "insta-app" and click "Register app".
14. In the "Add Firebase SDK" section, click "Use npm".
15. Replace the `const firebaseConfig` with your own Firebase configuration values in the `.env` file.


To run this project, you need to add the following environment variables to your `.env` file:

```
REACT_APP_API_KEY=your firebase apiKey
REACT_APP_AUTH_DOMAIN=your firebase authDomain
REACT_APP_PROJECT_ID=your firebase projectId
REACT_APP_STORAGE_BUCKET=your firebase storageBucket
REACT_APP_MESSAGING_SENDER_ID=your firebase messagingSenderId
REACT_APP_APP_ID=your firebase appId
```

Replace `your firebase ...` with your Firebase app's actual configuration values.

### next-auth Setup

1. Make sure the `next-auth` package is installed (it should be listed in your `package.json` file).
2. Look for the `auth` folder in your project directory and open the `[...nextauth].js` file.
3. This file should contain the following environment variables:
   ```javascript
   clientId: process.env.GOOGLE_CLIENT_ID,
   clientSecret: process.env.GOOGLE_CLIENT_SECRET,

   In Firebase: 
1. Navigate to "Authentication" and then to the "Sign-in method".
2. Click on "Google" under the Sign-in providers.
3. Click on "Web SDK configuration".
4. Copy the "Web client ID" and "Web client secret".
5. Paste these values into the `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` fields respectively in your `.env.local` file. Make sure to remove any spaces around the equals sign (=).

1. Create a .env.local file in the root directory of your project if it doesn't exist already.
2. Add the following environment variables to your .env.local file:
makefile
Copy code
GOOGLE_CLIENT_ID=<your_web_client_id>
GOOGLE_CLIENT_SECRET=<your_web_client_secret>
NEXTAUTH_URL=http://localhost:3000

### Installation

1. Clone the repository:

```bash
git clone https://github.com/MrPiccolo23/InstagramClone2.0.git
```

2. Navigate to the project directory:

```bash
cd [Your Project Folder Name]
```

3. Install the dependencies:

```bash
npm install
```

or if you are using yarn:

```bash
yarn install
```


### Run Locally

start the application in development mode, run:


npm run dev
The application will be accessible at http://localhost:3000. You should see the following in your terminal:

ready - started server on 0.0.0.0:3000, url: http://localhost:3000
info  - Loaded env from C:\Users\Sattar\Desktop\insta-2-yt\.env.local
info  - Loaded env from C:\Users\Sattar\Desktop\insta-2-yt\.env

