# Todo Application

A full-stack Todo application built with Django (backend) and React (frontend).

## Features

- Create, read, update, and delete todos
- Mark todos as complete/incomplete
- Filter todos by status (All, Pending, Completed)
- Responsive design
- Real-time updates

## Tech Stack

### Backend
- Django 5.2
- Django REST Framework
- SQLite database
- CORS headers for cross-origin requests

### Frontend
- React 18.2.0
- Axios for API calls
- React Icons for UI elements
- SCSS for styling

## Prerequisites

- Python 3.13 or higher
- Node.js and npm
- Git

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd todo-app
```

2. Set up the backend:
```bash
cd backend
pip install django djangorestframework django-cors-headers
python manage.py migrate
python manage.py createsuperuser  # Follow prompts to create admin user
```

3. Set up the frontend:
```bash
cd frontend
npm install
```

## Running the Application

1. Start the backend server:
```bash
cd backend
python manage.py runserver
```
The backend will run on http://localhost:8000

2. Start the frontend development server:
```bash
cd frontend
npm start
```
The frontend will run on http://localhost:3000 (or the next available port)

## Admin Access

The application comes with a pre-configured admin user:

- Username: `admin`
- Password: `admin123`

To access the admin interface:
1. Navigate to http://localhost:8000/admin
2. Log in with the credentials above

## API Endpoints

- GET /api/todos/ - List all todos
- POST /api/todos/ - Create a new todo
- GET /api/todos/{id}/ - Get a specific todo
- PUT /api/todos/{id}/ - Update a todo
- DELETE /api/todos/{id}/ - Delete a todo
- PATCH /api/todos/{id}/toggle/ - Toggle todo completion status
- GET /api/todos/{value}/filter/ - Filter todos by status (0 for pending, 1 for completed)

## Project Structure

```
todo-app/
├── backend/
│   ├── api/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py
│   │   └── urls.py
│   └── backend/
│       ├── settings.py
│       └── urls.py
└── frontend/
    ├── src/
    │   ├── app.js
    │   ├── app.scss
    │   └── index.js
    └── package.json
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

Maintained by Pujari Yaswanth Sai