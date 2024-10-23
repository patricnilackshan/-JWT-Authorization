# Simple Express JWT Authentication

This is a simple Express.js application that demonstrates JWT authentication. Users can log in to receive a token that allows them to access protected routes.

## Features

- User login with JWT token generation.
- Protected route to fetch user-specific posts.

## Technologies Used

- Node.js
- Express
- JWT (JSON Web Tokens)
- EJS (Embedded JavaScript Templates)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/patricnilackshan/JWT-Authorization.git
   ```

2. Navigate to the project directory:

    ```bash
    cd JWT-Authorization
    ```

3. Install dependencies:

    ```bash
    npm install
    ```

4. Create a .env file in the root of the project and add your JWT secret:

    Code to generate a `random_secret` in node terminal
    ```js
    require('crypto').randomBytes(64).toString('hex')
    ```

    .env
    ```plaintext
    ACCESS_TOKEN_SECRET=<random_secret>
    ```

5. Running the Application
    To start the server, run:

    ```bash
    npm run dev
    ```
    
The server will be running on http://localhost:3001.

## Usage
Navigate to http://localhost:3001/login to access the login page.

Enter your username and click "Login" to receive a JWT token.

Use the token in the Authorization header to access protected routes, such as /posts.

Testing the API
You can use the provided requests.rest file for testing the API with various HTTP requests.