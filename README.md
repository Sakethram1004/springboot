# springboot

# To-Do List Application

A simple Spring Boot application that provides a REST API for managing a basic To-Do list. The API supports adding, updating, viewing, and deleting tasks.

---

## Technologies Used
- **Spring Boot**: Backend framework for building the REST API.
- **H2 Database**: In-memory database for storing tasks.
- **Maven**: Dependency management and build tool.
- **Postman**: Tool for testing the API endpoints.

---

## Setup and Installation
1. **Prerequisites**:
   - Java JDK 11 or higher.
   - Maven 3.x.x.
   - Git (optional).

## 2. **Clone the Repository**:
   - git clone https://github.com/your-username/todo-app.git
   - cd todo-app
    
## 3. **Build the Project**:
   - mvn clean install

----
## Running the Application

**Start the application:
- mvn spring-boot:run
** The application will be available at:
- http://localhost:8080

----

## API Endpoints

Base URL: http://localhost:8080


-- HTTP Method	      -- Endpoint	                    --   Description	                     --  Request Body (JSON) Example
1. GET	            * /tasks	                       * Get all tasks.	                     * N/A
2. GET	            * /tasks/{id}	                 * Get a specific task by ID.	         * N/A
3. POST	            * /tasks	                       * Add a new task.	                     * {"title": "Task 1", "description": "Do something", "completed": false}
4. PUT	            * /tasks/{id}	                 * Update an existing task by ID.	      * {"title": "Updated Task", "description": "Updated description", "completed": true}
5. DELETE	         * /tasks/{id}	                 * Delete a task by ID.	               * N/A

---- 
## Testing the API

1. Use Postman or any API testing tool to test the endpoints.
2. Example requests:
- Add a Task:
POST http://localhost:8080/tasks
** Body:
{
  "title": "Complete Spring Boot Task",
  "description": "Finish the To-Do list application",
  "completed": false
}
- View All Tasks:
GET http://localhost:8080/tasks
- Update a Task:
PUT http://localhost:8080/tasks/1
Body:
{
  "title": "Updated Task",
  "description": "This task has been updated",
  "completed": true
}
- Delete a Task:
DELETE http://localhost:8080/tasks/1
