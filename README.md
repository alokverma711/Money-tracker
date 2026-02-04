# MoneyNotes 🧾

MoneyNotes is a modern, AI-powered expense tracker designed to help you understand your spending habits with ease. Built with React, Django, and Google Gemini AI, it offers a seamless experience for tracking expenses, categorizing transactions, and gaining personalized financial insights.


---

## ✨ Features

* **🤖AI-Powered Insights**: Get personalized financial advice and spending analysis powered by Google Gemini.
* **🧠Smart Categorization**: Automatically categorizes your expenses based on descriptions using AI if the category is left empty.
* **🪟Real-time Dashboard**: View your total spending, top category, total number of expenses, and spending trends using a graph.
* **📊Finance Assistant (AI Agent)**: An AI agent acts as your finance assistant and:
  - Gives monthly / weekly insights  
  - Compares your spending with previous periods  
  - Provides money-saving suggestions
* **🔐 Industrial Authentication**: Secure sign-in via **Clerk**, supporting traditional email and Google OAuth.
* **🖥️Responsive Design**: A clean, modern UI with dark and light mode support. Desktop-first with basic mobile responsiveness.
* **🔍Flexible Filtering**:
  - Weekly / Monthly toggle  
  - Custom date range filter (from – to)  
  - Search by description  
  - All-time expenses view
* **✏️Editable Expenses**: Edit description and category of any expense.
* **🗑️Delete Expenses**: Delete the expenses if you want to.
* **➕Floating Add Button**: Add new expenses using a floating action button.
* **🌓 Dark Mode/Light Mode**: A beautiful, responsive UI designed for a modern aesthetic across all devices.

---

## 🛠️ Tech Stack

*   **Frontend**: React, Vite, Axios, Clerk React SDK
*   **Backend**: Django, Django REST Framework
*   **AI**: Google Gemini API
*   **Database**: MySQL (hosted in Aiven)
*   **Styling**: Custom CSS with dark/light mode support and a focus on modern aesthetics
*    **Deployment**:
  - Backend: Render  
  - Frontend: Vercel

---

## ⚡Prerequisites

Before you begin, ensure you have the following installed:

*   **Node.js** (v18 or higher)
*   **Python** (v3.10 or higher)
*   **Git**
*   **A MySQL Instance** (via Aiven.io or local)

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <repository-url>
cd MoneyNotes
```

### 2. Backend Setup (Django)

Navigate to the `tracker` directory:

```bash
cd tracker
```

Create and activate a virtual environment:

```bash
# Windows
python -m venv .venv
.\.venv\Scripts\Activate

# macOS/Linux
python3 -m venv .venv
source .venv/bin/activate
```

Install Python dependencies:

```bash
pip install -r requirements.txt
```

Set up environment variables:
Create a `.env` file in the `tracker` directory and add your keys:

```env
GOOGLE_API_KEY=your_google_gemini_api_key
GEMINI_API_KEY= same as GOOGLE_API_KEY
CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
DJANGO_SECRET_KEY=your_django_secret
```

Run migrations and start the server:

```bash
python manage.py migrate
python manage.py runserver
```

The backend will be running at `http://127.0.0.1:8000`.

### 3. Frontend Setup (React)

Open a new terminal and navigate to the `Frontend/expense-frontend` directory:

```bash
cd Frontend/expense-frontend
```

Install Node dependencies:

```bash
npm install
```

Set up environment variables:
Create a `.env` file in the `Frontend/expense-frontend` directory:

```env
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
VITE_API_BASE_URL=http://127.0.0.1:8000
```

Start the development server:

```bash
npm run dev
```

The frontend will be running at `http://localhost:5173` (or similar).

---

## 📖 Usage

1. **Sign In**: Use the Sign In button to authenticate via Clerk (email or Google).
2. **Add Expense**: Click the floating "+" button to add a new expense. Enter the amount and description. The category is optional — AI will auto-categorize if left empty.
3. **View Dashboard**: See total spending, trends, top category, and number of expenses.
4. **Insights**: View AI-generated insights and comparisons for weekly or monthly periods.
5. **Filter & Search**:
   * Filter by date range
   * Toggle weekly / monthly
   * View all-time expenses
   * Search by description
7. **Edit Expense**: Use the edit button next to any expense to modify details.
8. **Theme Toggle**: Switch between dark and light mode.

---

## 🔮 AI Usage Note

MoneyNotes uses Google Gemini for:
  * Insights 
  * Category seggestion
**Note**: AI features are rate-limited on the free tier.
When limits are reached, the application gracefully falls back without breaking core functionality.

---

## 📚 What I Learned & Challenges Overcome
  * How to build a backend using Django REST Framework
  * How to build a working frontend using React
  * How to connect frontend and backend
  * How authentication works in real applications
  * How to use databases properly in full-stack projects
  * How to integrate AI using APIs
  * How to deploy backend and frontend
  * How to debug network, CORS, and deployment issues
  * How to handle AI limits and errors gracefully

---

## 📄License

This project is open-source and available under the MIT License.
