# Platform Service Incident Tracker

A modern, user-friendly web application built with Python Flask to track platform service incidents and manage server inventory. Say goodbye to Excel spreadsheets and hello to an intuitive interface that improves data management, accessibility, and usability.

## 🚀 Features

- **Incident Tracking**: Log and manage incidents with details like serial number, issue start/resolve times, host info, and more.
- **Server Inventory Management**: Maintain a detailed server inventory with fields like hostname, serial, brand, and specs.
- **Awesome UI/UX**: Built with Tailwind CSS for a clean, responsive, and customizable design.
- **Robust Backend**: Powered by Flask and Flask SQLAlchemy for reliable data handling.
- **Form Validation**: Intuitive forms with validation to ensure data accuracy.
- **Simple Deployment**: Easy setup for both local development and production.

## 🛠️ Tech Stack

- **Flask**: Lightweight and flexible Python web framework.
- **Flask SQLAlchemy**: Seamless database integration.
- **Flask-WTF**: Form handling and validation made easy.
- **Tailwind CSS**: Utility-first CSS framework for modern, responsive UI.
- **SQLite**: Lightweight database (with easy migration to PostgreSQL).

## 📦 Installation

Get started locally with these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/pesnik/platform-service-incident-tracker.git
   cd platform-service-incident-tracker
   ```

2. **Set Up a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   Ensure you have a `requirements.txt` file, then run:
   ```bash
   pip install -r requirements.txt
   ```

   Example `requirements.txt`:
   ```
   flask
   flask-sqlalchemy
   flask-wtf
   ```

4. **Initialize the Database**:
   ```bash
   flask db init
   flask db migrate
   flask db upgrade
   ```

5. **Run the Application**:
   ```bash
   flask run
   ```

6. **Access the App**:
   Open your browser at `http://127.0.0.1:5000/`.

## 🖥️ Usage

- **Home Page**: See an overview of incidents and server inventory.
- **Incidents**: Go to `/incidents` to view, add, or edit incident records.
- **Servers**: Visit `/servers` to manage server inventory.
- **Add Entries**: Click "Add" to create new incidents or servers with validated forms.
- **Edit Entries**: Use "Edit" next to any entry to update details.

The Tailwind CSS-powered interface is designed for simplicity and speed, making it a breeze to switch from Excel to this dynamic platform.

## 🎨 Customization

Make it your own:

- **Database Models**: Edit `app/models.py` to tweak incident or server fields.
- **Forms**: Adjust `app/forms.py` for custom fields or validation.
- **UI Styling**: Use Tailwind CSS in templates for styling or layout changes.
- **Routes**: Modify `app/views.py` to add new features.

After model changes, update the database:
```bash
flask db migrate
flask db upgrade
```

## 🚀 Deployment

For production:
- Use Gunicorn and NGINX for performance.
- Switch to PostgreSQL for scalability if needed.
- Example Gunicorn command:
  ```bash
  gunicorn --workers 3 wsgi:app
  ```

Check the [Flask Deployment Guide](https://flask.palletsprojects.com/en/stable/deploying/) for more.

## 🤝 Contributing

We’d love your help! To contribute:
1. Fork the repo.
2. Create a branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add cool feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

Stick to Python and Flask coding conventions.

## 📝 License

Licensed under the MIT License. See [LICENSE](LICENSE) for details.

## 🙏 Acknowledgments

- [Flask](https://flask.palletsprojects.com/) for the framework.
- [Tailwind CSS](https://tailwindcss.com/) for the sleek UI.
- [Flask SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/) and [Flask-WTF](https://flask-wtf.readthedocs.io/) for backend power.
