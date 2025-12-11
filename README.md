# 🎭 Moody - Real-time Mood Journal

**Moody** is a responsive web application that allows users to track their daily moods and write journal entries. It serves as a practical implementation of **Firebase v9** (Modular SDK) using Vanilla JavaScript.

## 🚀 Features

* **Authentication**:
    * Sign in with **Google** (Popup).
    * Create Account / Sign in with **Email & Password**.
    * Dynamic UI changes based on auth state (Logged In vs. Logged Out).
* **Mood Tracking**: Select from 5 mood levels (Awful to Amazing).
* **CRUD Operations**:
    * **Create**: Post new journal entries with a specific mood.
    * **Read**: Real-time fetching of posts.
    * **Update**: Edit existing journal entries.
    * **Delete**: Remove entries from the database.
* **Advanced Filtering**:
    * Filter posts by **Today**, **Week**, **Month**, or **All Time**.
    * Uses Firestore `query`, `where`, and `orderBy` for server-side filtering.

## 🛠️ Tech Stack

* **Frontend**: HTML5, CSS3 (Flexbox, CSS Variables), JavaScript (ES6 Modules).
* **Backend / BaaS**: Firebase.
    * **Firebase Auth**: User management.
    * **Cloud Firestore**: NoSQL Database for storing posts.

## ⚙️ Setup & Configuration

To run this project locally, you need your own Firebase project.

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/yourusername/moody-firebase-journal.git](https://github.com/yourusername/moody-firebase-journal.git)
    ```
2.  **Create a Firebase Project**:
    * Go to the [Firebase Console](https://console.firebase.google.com/).
    * Create a new project.
    * Enable **Authentication** (Google & Email/Password providers).
    * Enable **Cloud Firestore** (Start in Test Mode).
3.  **Update Configuration**:
    * Open `index.js`.
    * Replace the `firebaseConfig` object with your own keys:
    ```javascript
    const firebaseConfig = {
      apiKey: "YOUR_API_KEY",
      authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
      projectId: "YOUR_PROJECT_ID",
      storageBucket: "YOUR_PROJECT_ID.firebasestorage.app",
    };
    ```
4.  **Run the App**:
    * Since this project uses ES6 Modules (`type="module"`), you must run it using a local server.
    * If using VS Code, use the **Live Server** extension.

## 📄 Concepts Applied

* **Firebase Modular SDK**: Importing only specific functions (`getAuth`, `onSnapshot`, etc.) to optimize performance.
* **State Management**: Handling `moodState` and UI filters using JavaScript variables.
* **DOM Manipulation**: Dynamically creating HTML elements (`div`, `img`, `button`) based on database data.
* **Date Manipulation**: Calculating timestamps for "Today", "Week", and "Month" filters.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
