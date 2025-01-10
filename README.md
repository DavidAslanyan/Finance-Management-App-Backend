# MoneyCounter Backend - Financial Management API

**MoneyCounter Backend** is a robust API built with **Python**, **Flask**, **PostgreSQL**, and **Redis** to help users efficiently manage their financial transactions. This backend provides **CRUD operations** for managing income and expenses, ensuring secure and fast access to your financial data.

## Setup & Installation

### Prerequisites

- **Python 3.x**: Ensure you have [Python 3.x](https://www.python.org/downloads/) installed.
- **PostgreSQL**: Make sure you have [PostgreSQL](https://www.postgresql.org/) installed and running.
- **Redis**: Install and run [Redis](https://redis.io/) for session management and caching.

### Steps to Get Started

1. **Clone the repository**:
    ```bash
    git clone https://github.com/DavidAslanyan/Finance-Management-App-Backend.git
    ```
2. **Navigate to the project directory**:
    ```bash
    cd MoneyCounter-backend
    ```

3. **Create a virtual environment** (optional but recommended):
    ```bash
    python3 -m venv venv
    ```

4. **Activate the virtual environment**:
    - On Windows:
        ```bash
        venv\Scripts\activate
        ```
    - On Mac/Linux:
        ```bash
        source venv/bin/activate
        ```

5. **Install the dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

6. **Set up PostgreSQL Database**:
    - Create a new PostgreSQL database (e.g., `moneycounter`).
    - Update the `DATABASE_URI` in the `config.py` with the correct database connection string.

7. **Run Database Migrations**:
    ```bash
    flask db upgrade
    ```

8. **Start the Flask Development Server**:
    ```bash
    flask run
    ```

    The API will now be running at [http://localhost:5000](http://localhost:5000).


## Features

- **User Authentication**: Utilizes **Redis** for secure authentication and session management.
- **CRUD Operations**: Perform Create, Read, Update, and Delete actions on financial transactions.
- **Transaction Management**: Manage income and expense records with customizable fields.
- **Secure Data Handling**: Ensures all user data is stored securely in **PostgreSQL**.
- **Session Management**: Sessions are efficiently managed and stored using **Redis** for fast access.

## Tech Stack

- **Python**: A powerful and flexible programming language.
- **Flask**: A lightweight WSGI web application framework for building APIs.
- **PostgreSQL**: A robust relational database management system for storing user and transaction data.
- **Redis**: A fast, open-source key-value database used for caching and session management.
- **SQLAlchemy**: ORM for interacting with the PostgreSQL database in a Pythonic way.
- **JWT**: JSON Web Tokens used for secure user authentication and session management.

## Endpoints

### Authentication

- **POST /login**: User login with email and password. Returns a JWT token.
- **POST /register**: User registration with email, password, and username.

### CRUD Operations for Transactions

- **GET /transactions**: Retrieve all financial transactions.
- **GET /transactions/{id}**: Retrieve a specific transaction by its ID.
- **POST /transactions**: Add a new transaction (income or expense).
- **PUT /transactions/{id}**: Update an existing transaction by ID.
- **DELETE /transactions/{id}**: Delete a specific transaction by ID.

### Other Endpoints

- **GET /balance**: Get the current balance (sum of income and expenses).
- **GET /categories**: Get a list of transaction categories (e.g., "Food", "Rent", etc.).

## Environment Variables

Set the following environment variables before running the app:

- `FLASK_APP`: The entry point for your Flask application (e.g., `app.py`).
- `FLASK_ENV`: Set to `development` for development mode.
- `DATABASE_URI`: Connection string for the PostgreSQL database.
- `SECRET_KEY`: Flask secret key used for signing cookies and sessions.
- `REDIS_URL`: Connection string for the Redis server.

## Usage

- **Register** a new user or **login** to an existing one to start managing transactions.
- Use the **API** to interact with your transactions: add, edit, or delete.
- Fetch the **balance** to view your financial health.

## Contributing

Contributions are welcome! If you’d like to contribute, follow these steps:

1. Fork the repository.
2. Create a new feature branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -am 'Add new feature'`.
4. Push to your branch: `git push origin feature/your-feature`.
5. Create a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **Flask** for the powerful and lightweight framework that makes API development fast and efficient.
- **PostgreSQL** for providing a robust database solution for storing transaction data.
- **Redis** for efficient session management and caching.
- **SQLAlchemy** for making database interaction smooth and Pythonic.
