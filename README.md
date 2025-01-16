# Flask To-Do Application

A simple to-do list web application built with Flask and SQLite. Users can create, view, update, and delete tasks through an intuitive web interface.

## Features

- **Add Tasks**: Users can add new tasks to the to-do list.
- **View Tasks**: Display all tasks in chronological order.
- **Update Tasks**: Edit the content of existing tasks.
- **Delete Tasks**: Remove tasks from the list.
- **Database Integration**: Stores task data using SQLite.

## Tech Stack

- **Backend**: Flask
- **Database**: SQLite
- **Frontend**: HTML templates rendered using Flask

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/flask-todo-app.git
   cd flask-todo-app
   ```

2. **Set Up a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install flask flask_sqlalchemy
   ```

4. **Set Up the Database**:
   - Open a Python shell and run the following commands to create the database:
     ```python
     from app import db
     db.create_all()
     ```

5. **Run the Application**:
   ```bash
   python app.py
   ```

6. **Access the Application**:
   Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

## Project Structure

```
flask-todo-app/
├── app.py                # Main Flask application
├── templates/
│   ├── index.html        # Home page template
│   ├── update.html       # Task update page template
├── static/               # Static files (if any)
└── test.db               # SQLite database file (auto-generated)
```

## Routes

1. `/` (Home):
   - **GET**: Display all tasks.
   - **POST**: Add a new task.

2. `/delete/<int:id>`:
   - **GET**: Delete a task by its ID.

3. `/update/<int:id>`:
   - **GET**: Render the update form for a task.
   - **POST**: Save changes to the task.

## Future Enhancements

- Add user authentication to manage tasks per user.
- Include task priority levels.
- Add due dates and notifications for tasks.
- Improve the UI with a modern frontend framework (e.g., Bootstrap or Tailwind CSS).
