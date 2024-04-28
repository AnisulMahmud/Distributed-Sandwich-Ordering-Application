# Project Overview:

The project aims to develop a simple sandwich-ordering application with a focus on distributed components and communication. It comprises front-end, and back-end servers A and B, and a message broker for asynchronous communication. Docker containerization will be utilized for deployment.

## Overview of Sandwich Ordering Process:

1. User Interaction: Users use the frontend interface to order sandwiches from predetermined menu selections. Users get alerts including their unique order IDs after successfully placing their orders.
2. Communication: The frontend communicates sandwich orders via HTTP messages to Server A.
3. Server A Functionality: Server A handles incoming frontend messages, manages data storage for orders, and forwards orders to Server B through the message broker.
4. Database Integration: Server A integrates with a chosen database to store sandwich orders and pre-made sandwich types, facilitating efficient data management.
5. Backend Communication: Server B listens for new orders from the message broker, confirms order readiness, and communicates back to Server A.
6. User Notification: Server A updates order statuses, ensuring users are promptly notified of any changes in their order status via the frontend interface.

## Project Objectives:

Develop a user-friendly sandwich ordering application with features for placing orders, viewing all orders, and accessing specific orders by ID.
Use a message broker (RabbitMQ) to manage asynchronous server communication, together with distributed components such as the frontend, backend servers A and B.
Ensure the application architecture is scalable and maintainable by using Docker containerization to provide effective communication amongst remote components during deployment.
Integrate MongoDB as the chosen database for Server A to store sandwich orders and pre-made sandwich types for efficient data management.
Implement missing functionality for HTTP methods in Server A and Server B to ensure seamless communication and order processing between the frontend and backend.
Develop user-friendly frontend UI using React, React Router for routing, Fetch API for backend communication, and CSS for styling, with components including Home, OrderPage, NavBar, NotFoundPage, and OrderDetails.
Thoroughly test the application, including integration testing for backend components, end-to-end testing for the entire application flow, and integration testing for React components with external services.
Document the project architecture, implementation details, and deployment steps to facilitate knowledge transfer and future maintenance by team members or external stakeholders.

## Backend Technology Stack:

   Node.js: Used to develop Server A and Server B for efficient and scalable backend functionality.
   RabbitMQ: Utilized as the message broker to facilitate communication between servers, ensuring reliable message delivery.
   MongoDB: Chosen as the database solution for storing order data, offering flexibility and scalability for handling large volumes of data.
   Docker and Docker Compose: Employed for containerized deployment of backend components, ensuring consistency across environments and facilitating easy scaling and management.

## Frontend Technology Stack:

 React: This project is built using React, a popular JavaScript library for building user interfaces. React allows developers to create reusable UI components, manage component states, and efficiently update and render components in response to data changes.
 React Router: This library is used for handling routing in the application. It allows us to render different components based on the current URL path.
 Fetch API: The Fetch API is used for making HTTP requests to the backend server. It's a modern, promise-based API for making asynchronous HTTP requests in JavaScript
 CSS: CSS is used for styling the application.

## Deployment steps are: 

-> Installation: Install Docker Desktop.
-> Build the Docker images: Navigate to the root directory of your project in the terminal. Run the command docker-compose up --build. This will initiate the building process for Docker images of your backend servers and MongoDB database.
-> Start the Docker Containers: Docker Compose will automatically launch the Docker containers when the image creation is completed successfully. Your backend servers and MongoDB database are now operational within Docker containers. You can see this both in the terminal and on the Docker desktop. Additionally, make sure to check the status of all containers on a regular basis. Containers may stop working due to firewall settings or random internet access concerns. In such circumstances, just restart the stopped containers from Docker Desktop to restore regular operations.
-> Start the Frontend: After the backend, switch to the frontend directory in your terminal. Execute the command npm install to install the required node modules for the front end. Then, launch the frontend server by running npm run dev.
-> Access the application: Open a web browser and navigate to localhost:3000 (or the port specified for your frontend server, you can see that on the terminal). You should now have access to your sandwich ordering application's user interface.
-> Monitor the Application: Keep an eye on your terminal and Docker Desktop for any error messages or issues during the deployment process. 

## Application previews
### Home Page: 
![unnamed](https://github.com/AnisulMahmud/SandwichHub--Full-Stack-Sandwich-Ordering-System/assets/52384280/eca5aa80-10cb-4792-af08-7c3830a8eccb)

### Order List Page: 
![unnamed (1)](https://github.com/AnisulMahmud/SandwichHub--Full-Stack-Sandwich-Ordering-System/assets/52384280/deb6625d-21ab-477d-a24c-1db42e3c7050)

### Order Details Page: 

![unnamed (2)](https://github.com/AnisulMahmud/SandwichHub--Full-Stack-Sandwich-Ordering-System/assets/52384280/6d088385-76c5-4e97-99f7-542c0c466107)


## Future Development:
A whole sandwich ordering system will be the next target not just only the order. Check my other works too....




