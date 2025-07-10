# Django Login App

A modern, secure Django authentication system with a beautiful, responsive user interface built with Bootstrap 5.

## Features

- 🔐 **Secure Authentication**: Built with Django's robust authentication system
- 🎨 **Modern UI**: Beautiful, responsive design with Bootstrap 5 and Font Awesome icons
- 📱 **Mobile-First**: Fully responsive design that works on all devices
- ✨ **Gradient Design**: Eye-catching gradient backgrounds and glassmorphism effects
- 🔔 **Toast Messages**: User-friendly success and error messages
- 👤 **User Profile**: Detailed user profile page with account information
- 🛡️ **CSRF Protection**: Built-in security features
- 📝 **Form Validation**: Client-side and server-side form validation

## Screenshots

The app includes:
- **Home Page**: Welcome page with authentication status
- **Login Page**: Modern login form with validation
- **Signup Page**: User registration with Django's built-in UserCreationForm
- **Profile Page**: Detailed user information and account management
- **Navigation**: Responsive navbar with authentication-aware menu

## Quick Start

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Installation

1. **Clone the repository** (if you haven't already):
   ```bash
   git clone <your-repo-url>
   cd django-login-app
   ```

2. **Create and activate a virtual environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run database migrations**:
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser** (optional, for admin access):
   ```bash
   python manage.py createsuperuser
   ```

6. **Start the development server**:
   ```bash
   python manage.py runserver
   ```

7. **Open your browser** and visit: `http://127.0.0.1:8000`

## Usage

### Authentication Flow

1. **Visit the home page** - You'll see the welcome page with login/signup options
2. **Create an account** - Click "Sign Up" to create a new user account
3. **Login** - Use your credentials to sign in
4. **Access your profile** - View your account information and settings
5. **Logout** - Securely end your session

### Available URLs

- `/` - Home page
- `/accounts/login/` - Login page
- `/accounts/signup/` - User registration
- `/accounts/profile/` - User profile (requires login)
- `/accounts/logout/` - Logout
- `/admin/` - Django admin interface

## Project Structure

```
django-login-app/
├── loginapp/               # Main project directory
│   ├── settings.py        # Django settings
│   ├── urls.py           # Main URL configuration
│   └── wsgi.py           # WSGI configuration
├── accounts/              # Authentication app
│   ├── views.py          # View functions
│   ├── urls.py           # App URL patterns
│   └── apps.py           # App configuration
├── templates/             # HTML templates
│   ├── base.html         # Base template with Bootstrap
│   └── accounts/         # Account-specific templates
│       ├── home.html     # Home page
│       ├── login.html    # Login form
│       ├── signup.html   # Registration form
│       └── profile.html  # User profile
├── requirements.txt       # Python dependencies
├── manage.py             # Django management script
└── README.md            # Project documentation
```

## Customization

### Styling

The app uses Bootstrap 5 with custom CSS for:
- Gradient backgrounds
- Glassmorphism card effects
- Custom button animations
- Responsive design

You can customize the appearance by modifying the `<style>` sections in the templates.

### Authentication Settings

Key settings in `loginapp/settings.py`:
- `LOGIN_REDIRECT_URL = '/'` - Where to redirect after login
- `LOGOUT_REDIRECT_URL = '/'` - Where to redirect after logout
- `LOGIN_URL = '/accounts/login/'` - Login page URL

### Adding New Features

To extend the app:
1. Add new views in `accounts/views.py`
2. Create corresponding templates in `templates/accounts/`
3. Update URL patterns in `accounts/urls.py`

## Security Features

- CSRF protection on all forms
- Password validation (Django's built-in validators)
- Secure session management
- XSS protection through Django's template system
- SQL injection protection through Django ORM

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

If you encounter any issues or have questions, please:
1. Check the Django documentation: https://docs.djangoproject.com/
2. Review the code for examples and patterns
3. Create an issue on the repository

## Development

To set up for development:

```bash
# Clone and setup
git clone <your-repo-url>
cd django-login-app
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Database setup
python manage.py migrate
python manage.py createsuperuser

# Run development server
python manage.py runserver
```

Visit `http://127.0.0.1:8000` to see the application in action!

---

Built with ❤️ using Django and Bootstrap