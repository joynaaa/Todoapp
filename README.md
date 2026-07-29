# Todo Django Project

A complete todo application built with Django, featuring CRUD operations, templates, forms, and admin interface.

## Project Structure

```
todoproject/
├── todoproject/          # Main project settings
│   ├── settings.py      # Project configuration
│   ├── urls.py          # Project URL routing
│   └── wsgi.py
├── todos/               # Main app
│   ├── migrations/      # Database migrations
│   ├── templates/       # HTML templates
│   ├── models.py        # Todo model
│   ├── views.py         # Views (CRUD operations)
│   ├── forms.py         # TodoForm
│   ├── urls.py          # App URL routing
│   ├── admin.py         # Admin configuration
│   └── apps.py
└── manage.py
```

## Features

✅ **Create Todos** - Add new tasks with title and description
✅ **Read Todos** - View all todos in a list view
✅ **Update Todos** - Edit existing todos
✅ **Delete Todos** - Remove completed or unwanted todos
✅ **Mark Complete** - Toggle todo completion status
✅ **Admin Panel** - Manage todos from Django admin
✅ **Bootstrap UI** - Clean and responsive interface
✅ **Search & Filter** - Find todos in admin panel

## Models

### Todo
- `title` (CharField) - Task title (max 200 chars)
- `description` (TextField) - Task description (optional)
- `completed` (BooleanField) - Completion status
- `created_at` (DateTimeField) - Creation timestamp
- `updated_at` (DateTimeField) - Last update timestamp

## Getting Started

### 1. Install Dependencies
```bash
pip install django
```

### 2. Run Migrations
```bash
python manage.py migrate
```

### 3. Create Superuser (already done)
```bash
python manage.py createsuperuser
```
- Username: `admin`
- Password: `admin123`

### 4. Run Development Server
```bash
python manage.py runserver
```

The application will be available at: `http://127.0.0.1:8000/`

## URL Routes

| Route | Purpose |
|-------|---------|
| `/` | Todo list view |
| `/create/` | Create new todo |
| `/<id>/edit/` | Edit todo |
| `/<id>/delete/` | Delete todo |
| `/<id>/toggle/` | Mark todo as complete/incomplete |
| `/admin/` | Django admin panel |

## Admin Credentials
- **Username:** admin
- **Password:** admin123

## Views Used

- `TodoListView` - Display all todos (ListView)
- `TodoCreateView` - Create new todo (CreateView)
- `TodoUpdateView` - Edit todo (UpdateView)
- `TodoDeleteView` - Delete todo (DeleteView)
- `toggle_todo()` - Toggle completion status (Function-Based View)

## Forms

- `TodoForm` - ModelForm for Todo with Bootstrap styling

## Templates

- `base.html` - Base template with Bootstrap navbar
- `todo_list.html` - List all todos with action buttons
- `todo_form.html` - Create/Edit todo form
- `todo_confirm_delete.html` - Confirmation page before deleting

## Tips

1. **Todos are sorted** by creation date (newest first)
2. **Bootstrap 5** is used for styling
3. **CSRF protection** is enabled on all forms
4. **Auto-timestamps** are set for created and updated dates
5. **Admin panel** provides filtering and search capabilities

## Next Steps

- Add user authentication (multiple users)
- Add categories/tags for todos
- Add due dates and reminders
- Create a REST API with Django REST Framework
- Add pagination
- Add dark mode theme

Enjoy your todo app! 📝
