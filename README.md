# 🛒Mini E-Commerce Application

A minimal **React + Vite** project with **Tailwind CSS** and **Firebase** integration, designed to deliver high performance and fast development cycles. This project demonstrates key modern web development practices, including hot module replacement (HMR), optimized builds, and clean code with ESLint configurations.

## 📚Table of Contents

1. [Features](#features)
2. [Project Structure](#project-structure)
3. [Getting Started](#️getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
4. [Firebase Configuration](#firebase-configuration)
5. [Available Scripts](#available-scripts)
6. [ESLint Configuration](#️eslint-configuration)
7. [Contributing](#contributing)
8. [Creating Issues](#creating-issues)
9. [Acknowledgments](#acknowledgments)

## 🚀Features

- ⚡ **Vite**: Fast build tool with HMR for seamless development.
- ⚛️ **React 18**: Modern component-based UI library.
- 🎨 **Tailwind CSS**: Utility-first CSS framework for responsive designs.
- 🔥 **Firebase**: Integrated authentication and Firestore database.
- ✅ **ESLint**: Pre-configured for React with best practices and hooks rules.

## 📦Project Structure

```  
└── mini-e-commerce/  
    ├── README.md              # Project documentation and instructions  
    ├── README.old.md          # Previous version of the README for reference  
    ├── eslint.config.js       # Configuration file for ESLint (JavaScript linter)  
    ├── index.html             # Main HTML file for the application  
    ├── package.json           # Project metadata and dependencies  
    ├── vite.config.js         # Configuration file for Vite (build tool)  
    └── src/                   # Source files for the application  
        ├── App.jsx            # Main React component for the application  
        ├── main.jsx           # Entry point for the React application  
        ├── services/          # Directory for service-related files  
        │   └── firebase.js    # Firebase configuration and service functions  
        └── styles/            # Directory for styling files  
            └── index.css      # Main CSS file for application styles
```

## 🛠️Getting Started

### Prerequisites

- **Node.js** ≥ 16.x
- **Yarn** ≥ 1.22.x (recommended)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/mugabiBenjamin/mini-e-commerce.git
    cd mini-e-commerce

    # Install dependencies
    yarn install
    ```

2. Start the development server:
    ```bash
    yarn dev
    ```

## 🔥Firebase Configuration

1. Create a `.env` file in the root directory:
    ```env
    VITE_API_KEY=your_api_key
    VITE_AUTH_DOMAIN=your_auth_domain
    VITE_PROJECT_ID=your_project_id
    VITE_STORAGE_BUCKET=your_storage_bucket
    VITE_MESSAGING_SENDER_ID=your_messaging_sender_id
    VITE_APP_ID=your_app_id
    ```

2. Initialize Firebase services in `src/services/firebase.js`:
    ```javascript
    import { initializeApp } from "firebase/app";
    import { getAuth } from "firebase/auth";
    import { getFirestore } from "firebase/firestore";

    const firebaseConfig = {
        apiKey: import.meta.env.VITE_API_KEY,
        authDomain: import.meta.env.VITE_AUTH_DOMAIN,
        projectId: import.meta.env.VITE_PROJECT_ID,
        storageBucket: import.meta.env.VITE_STORAGE_BUCKET,
        messagingSenderId: import.meta.env.VITE_MESSAGING_SENDER_ID,
        appId: import.meta.env.VITE_APP_ID,
    };

    const app = initializeApp(firebaseConfig);
    export const auth = getAuth(app);
    export const db = getFirestore(app);
    ```

## 📋Available Scripts

- `yarn dev` → Runs the app in development mode with HMR.
- `yarn build` → Builds the app for production.
- `yarn preview` → Serves the production build locally.
- `yarn lint` → Runs ESLint for code quality checks.

## ⚙️ESLint Configuration

ESLint is pre-configured with the following plugins:

- `eslint-plugin-react`
- `eslint-plugin-react-hooks`
- `eslint-plugin-react-refresh`

Run the linter:
```bash
yarn lint
```

## 🤝Contributing

1. Fork the repository.
2. Create your feature branch:
    ```bash
    git checkout -b feature/awesome-feature
    ```
3. Commit your changes:
    ```bash
    git commit -m "Add awesome feature"
    ```
4. Push to the branch:
    ```bash
    git push origin feature/awesome-feature
    ```
5. Open a pull request.

## 🐛Creating Issues

If you encounter any bugs or have feature requests, please create an issue on the [GitHub Issues](https://github.com/mugabiBenjamin/mini-e-commerce/issues) page.

## 🌟Acknowledgments

- [Vite](https://vitejs.dev/)
- [React](https://reactjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Firebase](https://firebase.google.com/)

[🔝 Back to top](#mini-e-commerce-application)
