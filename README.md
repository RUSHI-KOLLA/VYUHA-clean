# VYUHA

VYUHA is a comprehensive, full-stack institution management system designed to streamline academic administration, including timetable scheduling, faculty leave management, room allocation, and subject management. It also features an AI-powered chat assistant to provide quick access to information and automated workflows.

## 🚀 Key Features

- **📅 Timetable Management**: Efficiently create, edit, and manage academic timetables.
- **🔄 Automated Substitution Engine**: Automatically handles faculty substitutions when leave is requested, minimizing classroom disruptions.
- **📝 Leave Management**: Streamlined workflow for faculty to request leaves and for administrators to manage them.
- **👥 User & Role Management**: Robust access control with roles such as Superadmin, Faculty, and others.
- **🏫 Room & Subject Management**: Centralized control over institutional resources including classrooms and academic subjects.
- **🤖 AI Chat Assistant**: An intelligent assistant to help users navigate the system and perform tasks via natural language.
- **🚩 Feature Flags**: Granular control over system features for staged rollouts and testing.
- **📊 Role-Based Dashboards**: Customized views and functionalities for different user types (e.g., Faculty Dashboard, Superadmin Panel).

## 🛠️ Tech Stack

### Backend
- **Language**: Python
- **API Framework**: Python-based API (FastAPI/Uvicorn)
- **Database & Auth**: [Supabase](https://supabase.com/)
- **Deployment**: Railway

### Frontend
- **Framework**: React
- **Build Tool**: Vite
- **Deployment**: Vercel
- **Client Library**: Supabase JS

## 🏗️ Architecture

VYUHA follows a modern client-server architecture:
- **Frontend**: A responsive React application that communicates with the backend through a RESTful API.
- **Backend**: A Python service that handles business logic, including complex engines for timetables and substitutions, and interacts with Supabase for data persistence and authentication.
- **Data Layer**: Supabase provides managed PostgreSQL database, real-time capabilities, and authentication services.

## 💻 Getting Started

### Prerequisites

- Python 3.x
- Node.js & npm
- A Supabase project

### Backend Setup

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/RUSHI-KOLLA/VYUHA-clean.git
    cd vyuha-clean/backend
    ```

2.  **Create a virtual environment**:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Configure environment variables**:
    Create a `.env` file in the `backend` directory and add your Supabase and other configuration details (see `backend/README.md` for full details).

5.  **Run the server**:
    ```bash
    python main.py
    ```
    The API will be available at `http://localhost:8000`.

### Frontend Setup

1.  **Navigate to the frontend directory**:
    ```bash
    cd ../frontend
    ```

2.  **Install dependencies**:
    ```bash
    npm install
    ```

3.  **Configure environment variables**:
    Create a `.env` file in the `frontend` directory and set `VITE_API_URL=http://localhost:8000`.

4.  **Run the development server**:
    ```bash
    npm run dev
    ```
    The frontend will be available at `http://localhost:5173`.

## 🌐 Deployment

- **Backend**: Deployable via Railway. Ensure all required environment variables are configured in the Railway dashboard.
- **Frontend**: Deployable via Vercel. Configure `VITE_API_URL` in the Vercel project settings to point to your deployed backend URL.

## 📁 Project Structure

```text
vyuha-clean/
├── backend/            # Python backend service
│   ├── tests/          # Backend test suite
│   ├── tools/          # Backend utility tools
│   ├── main.py         # API entry point
│   └── ...             # Core logic (engines, managers, etc.)
└── frontend/           # React frontend application
    ├── public/         # Static assets
    ├── src/            # Frontend source code
    │   ├── components/ # UI Components
    │   ├── lib/        # API and Supabase clients
    │   └── ...         # Main application logic
    └── ...             # Configuration files
```
