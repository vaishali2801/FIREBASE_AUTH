# Firebase Authentication 🔥

A simple authentication web application built with **React.js, Vite, and Firebase Authentication**. This project allows users to create an account using email and password and sign in with Google.

##screenshot


## 🚀 Features

- User registration with email and password
- User login with email and password
- Google sign-in authentication
- Firebase Authentication integration
- React-based user interface
- Fast development with Vite
- Environment variables for Firebase configuration

## 🛠️ Technologies Used

- React.js
- Vite
- JavaScript (ES6+)
- Firebase Authentication
- HTML5
- CSS3
- Bootstrap (if used in the project)

## 📁 Project Structure

```text
FIREBASE_AUTH/
├── public/
├── src/
│   ├── assets/
│   ├── auth/
|       |_AuthLogin.jsx
│   ├── config/
│   │   └── firebase.js
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .env
├── .gitignore
├── index.html
├── package.json
├── package-lock.json
├── vite.config.js
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/vaishali2801/FIREBASE_AUTH.git
```

Navigate to the project directory:

```bash
cd FIREBASE_AUTH
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Firebase

1. Open the [Firebase Console](https://console.firebase.google.com/).
2. Create a Firebase project or select an existing project.
3. Register a web application in Project Settings.
4. Copy the Firebase configuration values.
5. Navigate to **Build → Authentication → Sign-in method**.
6. Enable the **Email/Password** and **Google** providers if you want to support both login methods.

### 4. Configure Environment Variables

Create a `.env` file in the project root directory and add your Firebase configuration:

```env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
VITE_FIREBASE_APP_ID=your_app_id
```

Replace the placeholder values with the actual values from your Firebase web app configuration.

**Important:** Never commit your `.env` file to GitHub. Add it to `.gitignore`.

### 5. Start the Development Server

```bash
npm run dev
```

Open the local URL displayed in your terminal, usually:

```text
http://localhost:5173
```

## 🔐 Firebase Configuration

The Firebase configuration is maintained in `src/config/firebase.js`.

```javascript
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";

const firebaseConfig = {
  apiKey: import.meta.env.VITE_FIREBASE_API_KEY,
  authDomain: import.meta.env.VITE_FIREBASE_AUTH_DOMAIN,
  projectId: import.meta.env.VITE_FIREBASE_PROJECT_ID,
  storageBucket: import.meta.env.VITE_FIREBASE_STORAGE_BUCKET,
  messagingSenderId: import.meta.env.VITE_FIREBASE_MESSAGING_SENDER_ID,
  appId: import.meta.env.VITE_FIREBASE_APP_ID,
};

const app = initializeApp(firebaseConfig);

export const auth = getAuth(app);
```

## ▶️ Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Starts the development server |
| `npm run build` | Creates a production build |
| `npm run preview` | Previews the production build |

## 🧪 Testing

- Register a new user with a valid email address and password.
- Sign in with the registered credentials.
- Test Google sign-in after enabling the Google provider.
- Check Firebase Console → Authentication → Users to verify registered accounts.
- Inspect the browser console for authentication errors.

## 🔒 Security Notes

- Keep service-account private keys and server-side secrets out of frontend code.
- Do not log passwords or sensitive authentication data.
- Configure Firebase Security Rules appropriately for any database or storage services.
- Restrict API keys where appropriate.
- Remember that Vite exposes variables prefixed with `VITE_` to client-side code.

## 🚀 Production Deployment

You can deploy the application using services such as Vercel or Netlify.

1. Push your code to GitHub.
2. Import the repository into your hosting provider.
3. Add all required `VITE_FIREBASE_*` environment variables in the hosting dashboard.
4. Deploy the application.
5. Add the deployed domain to Firebase Authentication's authorized domains if required.

## 👩‍💻 Author

**Vaishali Chauhan**

B.Tech in Information Technology

## 📄 License

This project is available for educational and learning purposes. Add a specific open-source license if you intend to distribute it under one.
