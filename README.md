# Hospital Management System

A comprehensive Django REST Framework-based API for hospital management, including patient, doctor, appointment, and service management.

## Features

- **User Management**: Registration, authentication, and profile management
- **Patient Management**: Patient profiles and records
- **Doctor Management**: Doctor profiles, specializations, designations, and available times
- **Appointment System**: Schedule and manage appointments between patients and doctors
- **Review System**: Patient reviews for doctors
- **Service Management**: Hospital services information
- **Contact Management**: Contact form submissions

## Project Structure

The project is organized into several Django apps:

- `user_profile`: User authentication and profile management
- `patient`: Patient management
- `doctor`: Doctor management, including specializations, designations, and available times
- `appointment`: Appointment scheduling and management
- `service`: Hospital services information
- `contact_us`: Contact form submissions

## API Documentation

Comprehensive API documentation is available in the `docs/` directory:

- **OpenAPI Specification**: `docs/openapi.yaml`
- **API Guide**: `docs/api_guide.md`
- **Interactive Documentation**: `docs/swagger.html`

See the [Documentation README](docs/README.md) for more information.

## Installation

1. Clone the repository

```bash
git clone <repository-url>
cd hospital_management
```

2. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

4. Apply migrations

```bash
python manage.py migrate
```

5. Create a superuser

```bash
python manage.py createsuperuser
```

6. Run the development server

```bash
python manage.py runserver
```

## Authentication

The API uses JWT (JSON Web Token) authentication. To authenticate:

1. Obtain a token by sending a POST request to `/api/user/login/`
2. Include the token in the Authorization header for subsequent requests:
   ```
   Authorization: Bearer <your_access_token>
   ```

## License

[MIT License](LICENSE)