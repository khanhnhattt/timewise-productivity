# TimeWise (TW) Project

**TimeWise (TW)** is a web application developed as a Capstone Project (SEP490\_G85) at FPT University. The final report was completed in Hanoi, December 2024.

The vision for TimeWise is to help individuals and teams manage their time and projects more easily and effectively. It is designed to be a comprehensive tool that simplifies scheduling, improves productivity, and makes coordination hassle-free. TimeWise aims to fill the gap between conventional methods and the need for a single, easy-to-use platform that simplifies scheduling and project coordination.

## ✨ Key Features

TimeWise provides a comprehensive suite of features, with all major features implemented by Release 2.

| Feature ID | Feature | Description | Status |
| :--- | :--- | :--- | :--- |
| **FE-01** | **Authentication** | Manages user login and registration, ensuring secure access to the application, notably supporting authentication via **Google** (Connect with Google),-. | Fully implemented |
| **FE-02** | **Email Synchronisation** | Users can link and manage multiple emails in one account. | Fully implemented |
| **FE-03** | **Task/Schedule Management** | Enables users to manage and organise tasks and schedules efficiently, including creating, updating, tracking, and setting deadlines. | Fully implemented | 
| **FE-09** | **Workspace Management** | Allows users to manage and organize collaborative spaces, including creating, updating, deleting workspaces, inviting others, and setting member roles. | Fully implemented |
| **FE-04** | **AI Meeting Bot** | Assists users in scheduling and managing meetings by suggesting optimal times and handling conflicts. Automatically joins scheduled meetings, transcribes audio, and generates concise summaries. | Improvement needed |
| **FE-07** | **Real-Time Collaboration** | Enables users to collaborate on tasks, projects, and documents in real-time for seamless communication and coordination. | Fully implemented |
| **FE-08** | **File & Document Management** | Allows users to store, organise, and share important files within each workspace, centralizing project resources. | Fully implemented |
| **FE-06** | **Notifications & Alerts** | Provides real-time notifications for task updates, deadlines, and workspace changes. | Fully implemented |

## 💻 Technology Stack & Architecture

The system utilizes a modern microservices architecture and a web application structure (Next.js),, deployed primarily on Google Cloud Platform (GCP).

### Architecture Overview

| Component | Technology | Details | Source |
| :--- | :--- | :--- | :--- |
| **Architecture Design** | **Microservices** | Based on a multi-service structure including API, DMS, and AI Backend. | |
| **Frontend** | **Next.js** (React-based) | Front-end framework used for the client interface, fetches data from backend APIs. | [timewise-fe](https://github.com/timewise-team/timewise-fe/tree/cb389f4bf85351be9f6762b10a4328b1542ede8a) |
| **Backend (API/Logic)** | **Go Fiber (Go/Golang)** | API service layer handles business logic (running on port `:8000`). | [timewise-api](https://github.com/timewise-team/timewise-api/tree/9239052a56ce7515915103bbd009a62f05dd0bd7) |
| **Data Management Service (DMS)** | **Go** | Manages document storage and structured data interaction (running on port `:8089`). | [timewise-dms](https://github.com/timewise-team/timewise-dms/tree/147013f13dd28ff511ec58f2191d9c4241e98ac2) |
| **Database** | **MySQL** | Open-source relational database management system for structured data. | |
| **Storage** | **Google Cloud Storage** | Durable storage solution for unstructured data. | |
| **Messaging/Queue** | **RabbitMQ** | Message broker used for asynchronous task processing, such as the AI meeting bot tasks. | |
| **AI Integration** | **Gemini API** | Utilized for AI functionalities like generating meeting summaries. | [timewise-meeting-bot](https://github.com/timewise-team/timewise-meeting-bot/tree/e64f4dbbeb148b0fdeabeb6dc192f255bf8eb973) |
| **Deployment & CI/CD** | **GCP, Docker, Nginx, GitHub Actions** | Deployment uses Google Cloud Compute (GCE) Server, Docker for containerization, Nginx as a reverse proxy, and **GitHub Actions** for the CI/CD pipeline. |  |

## 🚀 Installation Summary (Deployment)

The comprehensive installation includes setting up the server, database, and integrating external services:

1.  Setup Google Cloud Compute (GCE) Server.
2.  Setup MySQL Container using Docker,.
3.  Setup Github Actions (for 3 Repositories) for continuous integration and deployment.
4.  Setup Domain/Cloudflare/Nginx.
5.  Install Frontend.
6.  Install Backend (including API, DMS, Meeting-Bot, and Notification services),.
7.  Setup Gemini API (retrieving and integrating the API Key),,.

## 👥 Project Team

This project was completed by Group G85 at FPT University (Semester Fall 2024).

| Name | Role in Report | **Key Individual Contributions** |
| :--- | :--- | :--- |
| Professor Thanh Hai To | Supervisor Professor | Provided invaluable advisory, guidance and consulting throughout the project's development. |
| **Nhat Khanh Hoang** | Leader, Product Owner, Fullstack Developer, Infrastructure | **Lead software architecture**, **Implement CI/CD**, **Fullstack Developer** (writing APIs, implementing Frontend, controlling FE/BE integration) |
| Bùi Lân Việt | Scrum Master, Back-end, Testing |
| Đinh Quang Thuận | Member, Back-end, Testing | 
| Nguyễn Đức Anh | Member, Front-end, Design |
| Nguyễn Gia Khánh | Member, Front-end, Design |
