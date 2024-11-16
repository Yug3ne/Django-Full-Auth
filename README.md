# Django-Full-Auth
This Django authentication tutorial demonstrates how to implement secure JWT authentication with cookie handling using the djoser library. The tutorial integrates JWT tokens with cookies, ensuring a stateless and secure authentication process. Additionally, SendGrid is used to handle email communications like account activation and password reset.
# Django JWT Authentication with Custom Cookie Handling

This repository demonstrates how to implement a custom JWT authentication flow in Django, focusing on token storage in secure HTTP-only cookies. It leverages the `djoser` library to manage user authentication while customizing token handling for improved security.

## Features:
- **Custom JWT Authentication**: Custom views to obtain, refresh, and verify JWT tokens.
- **Token Handling with Cookies**: Secure storage of `access` and `refresh` JWT tokens in cookies with HTTP-only, Secure, and SameSite attributes.
- **Automatic Token Management**: The backend handles token storage and renewal, simplifying frontend token management.
- **SendGrid Integration**: Email functionality for account activation and password reset using SendGrid.

## Key Components:
- `CustomTokenObtainPairView`: Handles user login and generates JWT tokens, setting them in cookies.
- `CustomTokenRefreshView`: Refreshes the JWT `access` token using the refresh token stored in cookies.
- `CustomTokenVerifyView`: Verifies the JWT `access` token from cookies to ensure the user's authentication.
- **Secure Cookie Settings**: Configurable settings for cookies, including SameSite, HTTP-only, and Secure attributes.

## Installation:
1. Clone the repository.
2. Install dependencies:
   ```pip install -r requirements```
3. Copy .env.local to .env ```cp .env.local .env ```Set up environment variables for API keys, like SENDGRID_API_KEY and FROM_EMAIL, in .env and Django settings.
4. Run migrations:
  ```python manage.py migrate  ```
5. Start the Django server:
   ``` python manage.py runserver ```
6. SendGrid Integration:
  This project uses SendGrid to handle email notifications, including account activation and password reset emails.
  resource ``` https://www.twilio.com/en-us/blog/email-activation-django-sendgrid ```

## Helpful Resources:
- https://djoser.readthedocs.io/en/stable/
- https://docs.djangoproject.com/en/stable/
