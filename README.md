✨ Task Manager App
A simple and elegant full-stack web application to manage your daily tasks. Stay organized and productive with this intuitive to-do list manager.

🌟 Features
Create, Read, Update, Delete (CRUD) Tasks: Easily add, edit, and remove tasks.

Modern UI: A clean, responsive, and visually appealing interface built with Bootstrap, featuring a "glassmorphism" effect.

Task Filtering: View all tasks, or filter by "completed" or "pending" status.

Dynamic Updates: The interface updates in real-time without needing to refresh the page.

Performance Optimized: Includes a simple caching mechanism to speed up task retrieval.

Persistent Storage: Tasks are saved in a MySQL database.

🛠️ Tech Stack
Frontend
HTML5

CSS3

JavaScript (ES6+)

Bootstrap 5 for responsive design and UI components.

Font Awesome for icons.

Backend
Python

Flask: A micro web framework for the backend server and REST API.

Flask-CORS: Handles Cross-Origin Resource Sharing.

Flask-Caching: Implements a simple in-memory cache.

mysql-connector-python: To connect the application with the MySQL database.

Database
MySQL

🚀 Getting Started
Follow these instructions to get a copy of the project up and running on your local machine.

Prerequisites
Python 3.x: Make sure you have Python installed. You can download it from python.org.

MySQL Server: You need a running instance of MySQL. You can download it from mysql.com.

pip: Python's package installer.

Installation & Setup
Clone the Repository

git clone [https://github.com/your-username/task-manager.git](https://github.com/your-username/task-manager.git)
cd task-manager

Create and Activate a Virtual Environment

On Windows:

python -m venv env
.\env\Scripts\activate

On macOS/Linux:

python3 -m venv env
source env/bin/activate

Install Dependencies
Install all the required packages using the requirements.txt file.

pip install -r requirements.txt

Configure the Database

Open the app.py file.

Modify the DB_CONFIG dictionary with your MySQL credentials:

DB_CONFIG = {
    'host': 'localhost',
    'user': 'your_mysql_username',
    'password': 'your_mysql_password',
    'database': 'todo_app'
}

The application will automatically create the todo_app database and the tasks table when you first run it.

Run the Application
Start the Flask development server:

python app.py

The application will be running at http://127.0.0.1:5000. Open this URL in your web browser.

📁 Project Structure
.
├── app.py              # Main Flask application file (backend logic)
├── requirements.txt    # Python dependencies
├── static/
│   ├── css/
│   │   └── style.css   # Custom styles for the frontend
│   └── js/
│       └── script.js   # Frontend JavaScript logic
└── templates/
    └── index.html      # Main HTML file for the user interface

📝 API Endpoints
The application exposes the following REST API endpoints:

GET /api/tasks: Fetches all tasks.

Query Parameters: filter (all, completed, pending)

POST /api/tasks: Creates a new task.

Body: { "title": "Task Title", "description": "Task Description" }

PUT /api/tasks/<int:task_id>: Updates an existing task.

Body: { "title": "Updated Title", "description": "Updated Description", "completed": true }

DELETE /api/tasks/<int:task_id>: Deletes a task.

Feel free to contribute to this project by forking it and creating a pull request.
