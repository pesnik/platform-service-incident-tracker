# Platform Service Incident Tracker

A modern, user-friendly web application built with Flask for the backend and React for the frontend to track platform service incidents and manage server inventory. Say goodbye to Excel spreadsheets and hello to an intuitive, dynamic interface that improves data management, accessibility, and usability.

## 🚀 Features

- **Incident Tracking**: Log and manage incidents with details like serial number, issue start/resolve times, host info, and more.
- **Server Inventory Management**: Maintain a detailed server inventory with fields like hostname, serial, brand, and specs.
- **Dynamic React Frontend**: A responsive and interactive interface built with React, enhancing user experience.
- **Robust Backend**: Powered by Flask and Flask SQLAlchemy for reliable data handling.
- **Form Validation**: Intuitive forms with validation to ensure data accuracy.
- **Simple Deployment**: Easy setup for local development and production.

## 🛠️ Tech Stack

- **Backend**:
  - Flask: Lightweight and flexible Python web framework.
  - Flask SQLAlchemy: Seamless database integration.
  - Flask-WTF: Form handling and validation made easy.
  - SQLite: Lightweight database (with easy migration to PostgreSQL).
- **Frontend**:
  - React: A JavaScript library for building user interfaces.
  - Create React App: Bootstrapping React projects quickly.
  - Tailwind CSS: Utility-first CSS framework for modern, responsive UI.

## 📦 Installation

Follow these steps to set up the project locally:

### 1. Clone the Repository

```bash
git clone https://github.com/pesnik/platform-service-incident-tracker.git
cd platform-service-incident-tracker
```

### 2. Set Up the Backend

#### Create and Activate a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

#### Install Python Dependencies

Ensure you have a `requirements.txt` file with:
```
flask
flask-sqlalchemy
flask-wtf
```

Then run:
```bash
pip install -r requirements.txt
```

#### Initialize the Database

```bash
flask db init
flask db migrate
flask db upgrade
```

### 3. Set Up the Frontend

#### Navigate to the Frontend Directory

```bash
cd frontend
```

#### Install Node Dependencies

Make sure you have [Node.js](https://nodejs.org/) installed, then run:
```bash
npm install
```

#### Run the React Development Server

```bash
npm start
```

This will start the React app, typically on `http://localhost:3000/`.

### 4. Run the Backend Server

In a separate terminal (with your virtual environment activated), run:

```bash
flask run
```

The Flask server will start on `http://127.0.0.1:5000/`.

## 🖥️ Usage

- **Home Page**: The React frontend provides an overview of incidents and server inventory.
- **Incidents**: Navigate to the incidents section to view, add, or edit incident records.
- **Servers**: Manage server inventory through the dedicated section.
- **Add/Edit Entries**: Use the React forms, which include validation, to create or update records. These forms communicate with Flask APIs in the backend.

## 🎨 Customization

Make it your own:

- **Backend Models**: Edit `app/models.py` to tweak incident or server fields.
- **API Endpoints**: Modify `app/views.py` to add new endpoints or features.
- **React Components**: Update components in the `frontend/src` directory for custom UI or logic.
- **UI Styling**: Use Tailwind CSS classes in React components for styling or layout changes.

After making any backend model changes, update the database:
```bash
flask db migrate
flask db upgrade
```

## 🚀 Deployment

For production deployment:

- **Backend**:
  - Use Gunicorn and NGINX for performance.
  - Switch to PostgreSQL for scalability if needed.
  - Example Gunicorn command:
    ```bash
    gunicorn --workers 3 wsgi:app
    ```
- **Frontend**:
  - Build the optimized React app:
    ```bash
    npm run build
    ```
  - Serve the static files with a web server or integrate them into your Flask app using a tool like WhiteNoise.

Refer to the [Flask Deployment Guide](https://flask.palletsprojects.com/en/stable/deploying/) and the [Create React App Deployment documentation](https://create-react-app.dev/docs/deployment/) for more details.

## 🤝 Contributing

We’d love your help! To contribute:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add cool feature'
   ```
4. Push to the branch:
   ```bash
   git push origin feature-branch
   ```
5. Open a pull request.

Please adhere to Python, Flask, and React coding conventions.

## 📝 License

Licensed under the MIT License. See [LICENSE](LICENSE) for details.

## 🙏 Acknowledgments

- [Flask](https://flask.palletsprojects.com/) for the backend framework.
- [React](https://reactjs.org/) for building the dynamic frontend.
- [Tailwind CSS](https://tailwindcss.com/) for the modern UI styling.
- [Flask SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/) and [Flask-WTF](https://flask-wtf.readthedocs.io/) for backend enhancements.
