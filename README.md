# Food Challenge

## Prerequisites

Ensure you have the following installed on your local machine:

- Docker
- Java JDK

## Setting Up Your Local Environment

1. **Clone the repository:**
    First, clone the `food-challenge` repository to your local machine. You can do this by running the following command in your terminal:

    ```bash
    git clone git@github.com:dvdonadelli/food-challenge.git
    ```

    Navigate to the project directory:

    ```bash
    cd food-challenge
    ```

2. **Start the PostgreSQL Database:**
    We're using Docker to run our PostgreSQL database. To start the database, ensure Docker is running and execute the following command:
   
    ```bash
    docker-compose up -d
    ```
3. **Run the Application:**
   With the database running, you can now start the application. We're using Gradle, and you can run the application using the following command:

    ```bash
    ./gradlew bootRun
    ```

That's it! Your local development environment is set up, and you should be able to start working on the project.


teste
