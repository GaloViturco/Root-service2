
# Login-Root Microservice 🚀

This microservice is part of the **Authentication-Domain** repository and is designed to handle the authentication and login process for the root user. It is built using Python and follows a microservices architecture with a focus on modularity and scalability.

## Repository Link 📁
- [GitHub Repository](https://github.com/GaloViturco/RootService)

## Docker Image 🐳
- **Docker Image:** `galo12/login-root`

## Purpose 🎯
This microservice facilitates user authentication for the root user, allowing secure login capabilities within the system. The service ensures that sensitive authentication details are handled securely, using industry best practices.

## Architecture Style 🏗️
- **Microservice Architecture:** This service is a standalone component that communicates with other services through defined APIs, making it independently deployable.
- **Design Pattern:** The service follows the **MVC (Model-View-Controller)** design pattern to separate concerns and ensure clean code structure.

## Technologies 💻
- **Programming Language:** Python 3.x
- **Framework:** Flask (for API routing and management)
- **Database:** SQL (integration via `db.py`)
- **Containerization:** Docker

## Project Structure 🧑‍💻
The repository is structured as follows:

```
Login-Root/
├── controllers/              # Contains logic for handling user requests.
│   └── login_controller.py   # Controller to manage the login process.
│
├── models/                   # Contains database models.
│   └── user_model.py         # Defines the user model, including authentication details.
│
├── routes/                   # API routes for authentication.
│   └── login_routes.py       # Routes to handle login-related API calls.
│
├── services/                 # Contains business logic services.
│   └── auth_service.py       # Service for processing authentication requests.
│
├── utils/                    # Utility functions and helper methods.
│   └── db.py                # Database connection and management.
│
├── app.py                    # Main application entry point.
├── Dockerfile                # Docker configuration for containerization.
├── README.md                 # This file.
└── requirements.txt          # Python dependencies for the project.
```

### Folder Descriptions 📂
- **controllers/**: Manages incoming requests and sends responses, following the MVC structure.
- **models/**: Contains the data models, primarily used to interact with the database.
- **routes/**: Handles the routes or endpoints that the microservice exposes.
- **services/**: Encapsulates the core business logic, like authentication.
- **utils/**: Houses utility functions like database connection handling (`db.py`).

## How to Deploy ⚙️
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/GaloViturco/RootService
   ```

2. **Install Dependencies:**
   Navigate to the project directory and install the necessary Python packages.
   ```bash
   pip install -r requirements.txt
   ```

3. **Docker Deployment:**
   - Build the Docker image:
     ```bash
     docker build -t galo12/login-root .
     ```
   - Run the container:
     ```bash
     docker run -p 5000:5000 galo12/login-root
     ```

4. **Access the Service:**
   - The service will be accessible on `http://localhost:5000` once the container is running.

## Features ✨
- **Login Management**: Facilitates secure login for the root user.
- **Modular and Scalable**: Designed to easily scale and integrate with other microservices.
- **Secure Authentication**: Follows security best practices for handling user credentials.

## Usage 📝
After deploying the microservice, make POST requests to `/login` with the root user's credentials to authenticate.

### Example POST Request:
```json
{
    "username": "root",
    "password": "yourpassword"
}
```

## License 📜
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
