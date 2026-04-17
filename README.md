# ðŸš€ Autonomous Systems Dashboard

The centralized master control panel for the Autonomous Systems agent ecosystem. This dashboard provides real-time visibility into AI token consumption, agent activity logs, and project portfolio management.

---

## ðŸŒŸ Key Features

- **Real-time AI Telemetry**: Live tracking of token usage and estimated costs for:
  - **OpenAI (GPT-4o)**
  - **Google Gemini (1.5 Pro)**
- **Agent Activity Log**: A streaming feed of actions and errors from your autonomous agents, ensuring transparency across the system.
- **Project Portfolio**: 
  - Manage and track discrete business projects.
  - Interactive "Flip Cards" for detailed technical configurations (Discord tokens, Gmail app passwords, etc.).
- **Google Sheets Sync**: One-click synchronization to ensure your local project data is mirrored in your master tracking spreadsheets.
- **Credential Management**: Guided tooltips and configuration paths for SMTP, Discord, and AI API keys.

---

## ðŸš€ Getting Started

### 1. Prerequisites
- **Python Backend**: The dashboard requires a local API server (usually running via `scripts/dashboard_server.py`) to serve metrics and handle project updates.
- **Data Files**: 
  - `usage.json`: Stores AI token telemetry.
  - `projects.json`: Stores persistent project data.

### 2. Running the Dashboard
1. Ensure your `.env` file is configured with the necessary keys.
2. Start the local server:
   ```bash
   python scripts/dashboard_server.py
   ```
3. Open `dashboard/index.html` in your browser (or access via the server URL, typically `http://localhost:5000`).

---

## ðŸ“‚ Project Structure

- `index.html`: The main dashboard interface using a premium "Glassmorphism" design and interactive 3D flip cards.
- `styles.css`: Custom CSS providing dark mode aesthetics, animated background orbs, and responsive grid layouts.
- `projects.json`: Local database for project tracking.
- `usage.json`: Live log of AI engine consumption.

---

## ðŸ› ï¸ Architecture

The dashboard is built as a hybrid system:
- **Frontend**: Modern HTML5/CSS3 and Vanilla JS for real-time DOM updates and animations.
- **Backend API**: A Python-based micro-service that bridges the local file system (logs/configs) with the web interface.

