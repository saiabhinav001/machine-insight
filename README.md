# MachineInsight - AI Predictive Maintenance Platform

**An enterprise-grade platform that leverages a cloud-hosted machine learning model to predict industrial equipment failures from real-time telemetry data.**

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![Vercel Deployment](https://img.shields.io/badge/Deployment-Vercel-black?logo=vercel)](https://machine-insight.vercel.app/)

---

### 🚀 **[Live Demo Link](https://machine-insight.vercel.app/)** 🚀

## 📸 Project Showcase

*A dynamic demonstration of the platform's features, from data input to receiving a live AI-powered prediction.*

MachineInsight Pro Live Demo

![Machine Insight](https://github.com/saiabhinav001/machine-insight/releases/download/v1.0.0-assets/MachineInsight.Live.Demo.gif)

---

## 📖 About The Project

MachineInsight Pro is a sophisticated web application designed to simulate and interact with a real-world predictive maintenance system. It provides an intuitive, glass-morphism interface for users to input sensor data—such as torque, temperature, and rotational speed—from industrial machinery. This data is then sent to a cloud-hosted XGBoost model deployed on IBM Watson Machine Learning to get a real-time prediction of potential equipment failures.

The platform was built to solve a critical business problem: **minimizing operational downtime and reducing maintenance costs.** By predicting failures before they happen, companies can move from a reactive to a proactive maintenance strategy, saving significant time and resources. This project demonstrates a full-stack development workflow, from an interactive frontend to a secure, scalable serverless backend proxy that protects sensitive API credentials.

---

## ✨ Key Features

* **Interactive UI:** A futuristic glass-morphism design with dynamic gauges, charts, and input fields for a seamless user experience.
* **Live AI Predictions:** Integrates directly with a cloud-hosted IBM Watson Machine Learning model to deliver predictions in real-time.
* **Secure API Handling:** Uses a Vercel Serverless Function as a backend proxy to securely manage and protect the IBM Cloud API key.
* **Real-time Analytics:** Features a dashboard with charts from Chart.js to visualize prediction trends and system health.
* **Advanced Animations:** Utilizes GSAP and custom CSS for smooth, engaging animations and transitions.
* **Fully Responsive:** Designed with Tailwind CSS to be perfectly usable on desktops, tablets, and mobile devices.

---

## 🛠️ Technology Stack & Architecture

This project was built using a modern, scalable tech stack.

### Frontend
| Technology | Description |
| :--- | :--- |
| **HTML5** | Semantic markup for application structure. |
| **Tailwind CSS** | A utility-first CSS framework for rapid, responsive UI development. |
| **JavaScript (ES6+)**| Handles all client-side logic, interactivity, and API communication. |
| **Chart.js** | Creates beautiful and interactive charts for data visualization. |
| **GSAP** | (GreenSock Animation Platform) Powers high-performance animations. |

### Backend & Deployment
| Technology | Description |
| :--- | :--- |
| **Vercel** | Platform for deploying the frontend and hosting serverless functions. |
| **Node.js** | The runtime environment for the serverless backend function. |
| **IBM Watson** | Cloud platform hosting the deployed XGBoost predictive model. |
| **GitHub** | Version control and CI/CD integration with Vercel. |

### 🏛️ Architectural Overview

The application follows a secure, decoupled architecture. The frontend, built with HTML, CSS, and JS, is completely static. All communication with the IBM Watson API is handled by a backend proxy.

1.  **Client (Browser):** The user inputs data and clicks "Analyze". The frontend sends a `POST` request to its own backend at `/api/predict`.
2.  **Vercel Serverless Function (Backend Proxy):** The `api/predict.js` function receives the request. It securely accesses the IBM API key from Vercel's environment variables.
3.  **IBM Watson API:** The serverless function calls the IBM API, sending the data and authenticating with the secret key.
4.  **Response Flow:** The prediction from IBM is returned to the serverless function, which then sends it back to the client to be displayed in the UI.

This architecture ensures that the **secret API key is never exposed in the browser**, solving the critical CORS and security issues inherent in client-side API calls.

### 📂 Project Structure
The project is organized with the frontend assets in the root and the serverless backend function in the `/api` directory, which is standard for Vercel deployments.
```
/
├── 📄 index.html
├── 📄 package.json
├── 📄 LICENSE.md
├── 📄 README.md
└── 📁 api/
    └── 📄 predict.js
```
---

## 🚀 Getting Started (Local Development)

To get a local copy up and running, follow these simple steps.

### Prerequisites
* Node.js (v18 or later)
* npm

### Installation
1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/YOUR_USERNAME/machine-insight.git](https://github.com/YOUR_USERNAME/machine-insight.git)
    ```
2.  **Navigate to the project directory:**
    ```sh
    cd machine-insight
    ```
3.  **Create a local environment file:**
    Create a file named `.env.local` in the root of your project and add your API credentials:
    ```
    WML_API_KEY="YOUR_IBM_CLOUD_API_KEY"
    WML_ENDPOINT_URL="YOUR_MODEL_ENDPOINT_URL"
    ```
4.  **Run the development server:**
    ```sh
    npx vercel dev
    ```
Your application will be running at `http://localhost:3000`.

---

## 📬 Contact

For any inquiries or feedback regarding this project, please feel free to reach out:

-   **Sai Abhinav Patel Sadineni**
-   **LinkedIn:** [linkedin.com/in/sai-abhinav-sadineni](https://www.linkedin.com/in/sai-abhinav-sadineni/)
-   **Email:** [abhinav.sadineni@gmail.com](mailto:abhinav.sadineni@gmail.com)

---

## 📄 License

This project is distributed under the MIT License. See the [LICENSE](https://github.com/saiabhinav001/machine-insight/blob/main/LICENSE.md) file for more information.
