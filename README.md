# 💼 GetaJob — AI-Powered Job & Interview Preparation Platform

<p align="center">
  <img src="https://raw.githubusercontent.com/halfrost/halfrost/master/icons/header_1.png" alt="banner" width="100%">
</p>

<h1 align="center">GetaJob</h1>

<p align="center">
  An AI-powered full-stack platform for job research, company insights, and personalized interview preparation.
</p>

<p align="center">
  <a href="https://github.com/YOUR_USERNAME/GetaJob">
    <img src="https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge&logo=github" alt="GitHub">
  </a>
</p>

---

## 📌 About The Project

**GetaJob** is a full-stack AI-powered job and interview preparation platform designed to help candidates prepare more effectively for their target companies and roles.

The platform combines **AI-powered interview preparation** with **company and job research** to provide candidates with personalized preparation material, interview questions, and relevant information.

GetaJob uses AI and web search capabilities to help users understand what to expect from a particular company or job role and prepare accordingly.

---

## ✨ Features

### 👤 User Features

- 🔐 User registration and authentication
- 👤 Personalized user experience
- 💼 Search and explore job opportunities
- 🏢 Research companies and their interview processes
- 🎯 Prepare for specific job roles
- 📚 Generate personalized interview preparation material
- 📝 AI-generated interview questions
- 📊 Personalized preparation resources
- 📱 Responsive user interface

### 🤖 AI Features

- 🧠 AI-powered interview preparation
- 💬 AI-generated interview questions
- 🎯 Role-specific preparation
- 🏢 Company-specific interview insights
- 📚 Personalized study and preparation plans
- 🔎 Web-powered company research
- ⚡ Dynamic AI-generated content

### 🔎 Job & Company Research

- 🏢 Company interview information
- 💼 Job role research
- 🔍 Web-based information retrieval
- 📋 Relevant interview preparation resources
- 🎯 Targeted preparation based on company and role

---

## 🛠️ Tech Stack

### Frontend

<p>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nextjs/nextjs-original.svg" width="50" height="50" alt="Next.js">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" width="50" height="50" alt="React">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" width="50" height="50" alt="JavaScript">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" width="50" height="50" alt="CSS3">
</p>

- Next.js
- React.js
- JavaScript
- HTML5
- CSS3
- Responsive Design

### Backend

<p>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" width="50" height="50" alt="Node.js">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" width="50" height="50" alt="Express.js">
</p>

- Node.js
- Express.js
- REST APIs
- Session-based authentication

### Database

<p>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" width="50" height="50" alt="MongoDB">
</p>

- MongoDB
- MongoDB Atlas

### AI & APIs

- 🤖 Groq
- 🔎 Tavily
- 🧠 Large Language Models
- 🌐 Web Search APIs

### Tools

- Git & GitHub
- VS Code
- Postman
- npm
- MongoDB Atlas

---

## 📂 Project Structure

```text
GetaJob/
│
├── server/
│   ├── src/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── .env.example
│   └── package.json
│
├── web/
│   ├── app/
│   ├── components/
│   ├── public/
│   ├── .env.local
│   └── package.json
│
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/GetaJob.git
```

### 2. Navigate into the project

```bash
cd GetaJob
```

---

### 3. Install Backend Dependencies

```bash
cd server
npm install
```

---

### 4. Configure Backend Environment Variables

Create a `.env` file inside the `server` directory.

Example:

```env
MONGODB_URI=your_mongodb_connection_string
SESSION_SECRET=your_session_secret

LLM_API_KEY=your_groq_api_key
LLM_PROVIDER=groq
LLM_MODEL=your_llm_model

SEARCH_API_KEY=your_tavily_api_key
```

> ⚠️ Never commit your `.env` file to GitHub.

---

### 5. Start Backend

```bash
npm run dev
```

The backend will run on the port configured by the application, typically:

```text
http://localhost:4000
```

---

### 6. Install Frontend Dependencies

Open another terminal:

```bash
cd GetaJob/web
npm install
```

---

### 7. Configure Frontend Environment Variables

Create:

```text
.env.local
```

Add:

```env
NEXT_PUBLIC_API_URL=http://localhost:4000
```

---

### 8. Start Frontend

```bash
npm run dev
```

The frontend will typically be available at:

```text
http://localhost:3000
```

---

## 🔐 Environment Variables

### Backend

| Variable | Description |
|---|---|
| `MONGODB_URI` | MongoDB database connection string |
| `SESSION_SECRET` | Secret used for session management |
| `LLM_API_KEY` | Groq API key |
| `LLM_PROVIDER` | LLM provider |
| `LLM_MODEL` | AI model used for generation |
| `SEARCH_API_KEY` | Tavily API key |

### Frontend

| Variable | Description |
|---|---|
| `NEXT_PUBLIC_API_URL` | URL of the backend API |

---

## ▶️ Running the Application

### Start Backend

```bash
cd server
npm run dev
```

### Start Frontend

Open another terminal:

```bash
cd web
npm run dev
```

Then open:

```text
http://localhost:3000
```

---

## 🔄 Application Workflow

```text
                ┌───────────────────┐
                │       User        │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │  Next.js Frontend │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Express.js Server │
                └─────────┬─────────┘
                          │
             ┌────────────┼────────────┐
             ▼            ▼            ▼
        ┌─────────┐  ┌─────────┐  ┌─────────┐
        │ MongoDB │  │  Groq   │  │ Tavily  │
        │Database │  │   AI    │  │ Search  │
        └─────────┘  └─────────┘  └─────────┘
```

---

## 🤖 AI-Powered Preparation

GetaJob uses AI to help candidates prepare according to their target role and company.

The platform can generate preparation resources such as:

- 📝 Interview questions
- 🎯 Role-specific preparation
- 🏢 Company-specific insights
- 📚 Study material
- 💡 Interview preparation guidance

---

## 🔎 Web Search Integration

The application uses **Tavily** to retrieve relevant web information.

This helps provide users with:

- Company information
- Interview-related information
- Job-specific research
- Relevant preparation resources

---

## 📸 Screenshots

### 🏠 Home Page

_Add your screenshot here._

```markdown
![Home Page](./screenshots/home.png)
```

### 💼 Job Search

_Add your screenshot here._

```markdown
![Job Search](./screenshots/jobs.png)
```

### 🤖 Interview Preparation

_Add your screenshot here._

```markdown
![Interview Preparation](./screenshots/interview-preparation.png)
```

### 📊 Dashboard

_Add your screenshot here._

```markdown
![Dashboard](./screenshots/dashboard.png)
```

---

## 🚀 Future Improvements

- 💼 Real-time job listings
- 📄 Resume analysis
- 🤖 AI resume improvement
- 🎤 AI mock interviews
- 🗣️ Voice-based interview practice
- 📊 Interview performance analytics
- 📧 Job application tracking
- 🔔 Job alerts
- ⭐ Company reviews
- 📱 Mobile application
- 💬 AI career assistant
- 📈 Personalized career recommendations

---

## 👨‍💻 Developer

**Yashraj Saini**

Full-Stack Developer | MERN | React | Node.js | AI

📍 Jaipur, India

- 💼 LinkedIn: [Yashraj Saini](https://www.linkedin.com/in/yashraj-saini-0aa230214/)
- 💻 GitHub: [YashSaini213](https://github.com/YashSaini213)
- 🌐 Portfolio: [My Portfolio](https://my-portfolio-zeta-murex-12.vercel.app/)
- 📧 Email: yashrajsaini713@gmail.com

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.

Thanks for checking out **GetaJob!** 🚀
