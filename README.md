# Todo App

This is a simple Todo App built using Next.js for the frontend, Node Express for the backend, and MongoDB for the database. The entire application is containerized using Docker for easy deployment and management.

## Getting Started

To run the Todo App locally, make sure you have Docker installed on your machine.

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/todo-app.git
   ```

2. Navigate to the project directory:

   ```bash
   cd todo-app
   ```

3. Build the Docker container:

   ```bash
   docker build -t todoapp .
   ```

4. Run the Docker container:

   ```bash
   docker run -p 3000:3000 -p 4000:4000 todoapp
   ```

   This command maps the container ports to the host machine, with the Todo App running on port 3000 and the backend on port 4000.

5. Access the Todo App in your web browser:

   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Backend: [http://localhost:4000](http://localhost:4000)


## Environment Variables

Ensure that you have a `.env` file in the `backend/` directory with the following variables:

```plaintext
MONGO_URI=<your-mongodb-connection-string>
```

Replace `<your-mongodb-connection-string>` with the connection string for your MongoDB instance.

## Docker Container Details

The Docker container is named `todoapp` and is built with the following specifications:

- **Exposed Ports:**
  - Frontend: 3000
  - Backend: 4000

## Notes

- Make sure to have Docker installed.
- Ensure that your MongoDB instance is accessible and replace the placeholder in the `.env` file.
- For production, consider using environment-specific configurations and securing sensitive information.

Feel free to customize the application according to your needs. Happy coding!
