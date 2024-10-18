# Course Management API

This project is a RESTful API for managing courses, built with Node.js, Express.js, and MongoDB. It provides CRUD (Create, Read, Update, Delete) operations for course management.

## Prerequisites

Before you begin, ensure you have met the following requirements:

* You have installed Node.js (version 12.x or later) and npm. You can download them from [nodejs.org](https://nodejs.org/).
* You have installed MongoDB (version 4.x or later). You can download it from [mongodb.com](https://www.mongodb.com/try/download/community).
* You have a GitHub account and Git installed on your local machine.
* You have a basic understanding of JavaScript and RESTful APIs.

## Cloning the Project

To clone this project, follow these steps:

1. Open your terminal (Command Prompt on Windows, Terminal on macOS or Linux).
2. Navigate to the directory where you want to clone the project.
3. Run the following command:

   ```bash
   git clone https://github.com/TheMarvelFan/Course-Api.git
   ```

4. Navigate into the project directory:

   ```bash
   cd Course-Api
   ```

## Setting Up the Project

After cloning the project, you need to set it up:

1. Install the project dependencies:

   ```bash
   npm install
   ```

2. Create a `.env` file in the root directory of the project:

   ```bash
   touch .env
   ```

3. Open the `.env` file in a text editor and add the following environment variables:

   ```
   MONGODB_URI=your_mongodb_connection_string_here
   PORT=3000
   ```

   Replace `your_mongodb_connection_string_here` with your actual MongoDB connection string.

## Running the Project

To run the project, follow these steps:

1. Make sure MongoDB is running on your machine.

2. Start the server:

   For production:
   ```bash
   npm start
   ```

   For development (with auto-restart on file changes):
   ```bash
   npm run dev
   ```

3. The server should now be running on `http://localhost:3000` (or the port you specified in the `.env` file).

## Testing the API

You can test the API using tools like [Postman](https://www.postman.com/) or `curl`. Here are the available endpoints:

- POST `/api/courses`: Create a new course
- GET `/api/courses`: Retrieve all courses
- GET `/api/courses/:id`: Retrieve a specific course by ID
- PUT `/api/courses/:id`: Update a course by ID
- DELETE `/api/courses/:id`: Delete a course by ID

Example of creating a new course using `curl`:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"title":"Introduction to Node.js","description":"Learn the basics of Node.js","duration":120}' http://localhost:3000/api/courses
```

## Adjustments and Customizations

1. **Database Connection**: If you're using a different MongoDB setup (like a remote database), make sure to update the `MONGODB_URI` in your `.env` file accordingly.

2. **Port**: The default port is set to 3000. If you need to use a different port, you can change it in the `.env` file.

3. **Course Model**: If you need to add or modify fields for the course model, you can do so in the `models/Course.js` file. Remember to update the corresponding route handlers in `routes/courses.js` if you make changes to the model.

4. **Error Handling**: The current implementation includes basic error handling. For a production environment, you might want to implement more robust error handling and logging.

5. **Authentication**: This API doesn't include authentication. For a production application, consider implementing user authentication and authorization.

6. **Validation**: You may want to add more detailed validation for course data. Consider using a library like `express-validator` for this purpose.

## Screenshots
- POST `/api/courses`:

![Screenshot 2024-10-19 003634](https://github.com/user-attachments/assets/fbbf604b-8deb-449d-9c64-6d01c3cbd820)

- GET `/api/courses`:

![Screenshot 2024-10-19 003657](https://github.com/user-attachments/assets/a000a444-94ba-4a74-813a-74840785e76f)

- GET `/api/courses/:id`:

![Screenshot 2024-10-19 003716](https://github.com/user-attachments/assets/74f0ba8b-4421-4242-a39d-aca0b0136e95)

- PUT `/api/courses/:id`:
https://github.com/user-attachments/assets/3f7fae07-9e3d-4af2-9738-28fa8ebdd86e

- DELETE `/api/courses/:id`:
https://github.com/user-attachments/assets/3ddf9e1a-7bb6-40f2-8cc6-89b62fd88ecc

