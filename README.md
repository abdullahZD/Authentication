# Authentication with Django Rest Framework

This is a simple Django Rest Framework project for handling user authentication. The project includes functionality for user registration, login, and logout using tokens.

## Getting Started

These instructions will help you set up the project locally for development and testing purposes.

### Prerequisites

- Python (3.6 or higher)
- Django
- Django Rest Framework

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/Authentication.git
    ```

2. Navigate to the project directory:

    ```bash
    cd Authentication
    ```

3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Apply database migrations:

    ```bash
    python manage.py migrate
    ```

5. Run the development server:

    ```bash
    python manage.py runserver
    ```

## Usage

### Register

Endpoint: `/api/register/`

#### Request

```http
POST /api/register/
Content-Type: application/json

{
  "username": "your_username",
  "password": "your_password",
  "email": "your_email@example.com"
}

Response
{
  "token": "your_access_token"
}


Login
Endpoint: /api/login/

Request
http
Copy code
POST /api/login/
Content-Type: application/json

{
  "username": "your_username",
  "password": "your_password"
}
Response
json
Copy code
{
  "token": "your_access_token"
}
Logout
Endpoint: /api/logout/

Request
POST /api/logout/
Authorization: Bearer your_access_token

Response
{
  "detail": "Successfully logged out."
}
