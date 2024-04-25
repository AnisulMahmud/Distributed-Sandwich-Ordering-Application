# Sandwich Ordering System -> Full Stack Web Application

The project aims to develop a simple sandwich-ordering application with a focus on distributed components and communication. It comprises front-end, and back-end servers A and B, and a message broker for asynchronous communication. Docker containerization will be utilized for deployment.

### Overview of Sandwich Ordering Process:

a. User Interaction: Users use the frontend interface to order sandwiches from predetermined menu selections. Users get alerts including their unique order IDs after successfully placing their orders.
b. Communication: The frontend communicates sandwich orders via HTTP messages to Server A.
c. Server A Functionality: Server A handles incoming frontend messages, manages data storage for orders, and forwards orders to Server B through the message broker.
d. Database Integration: Server A integrates with a chosen database to store sandwich orders and pre-made sandwich types, facilitating efficient data management.
e. Backend Communication: Server B listens for new orders from the message broker, confirms order readiness, and communicates back to Server A.
f. User Notification: Server A updates order statuses, ensuring users are promptly notified of any changes in their order status via the frontend interface.


### Backend Components - Server A and Server B:

a. Server A: Handles frontend messages, accesses data storage, sends orders to Server B, and implements the provided Swagger API.
b. Server B: Listens for new orders, confirms readiness, and communicates back to Server A.
c. Message Broker - RabbitMQ: Utilizes RabbitMQ with two message queues: one for communication between Server A and Server B.

### Frontend:
Developed with React, users may place orders, see all orders, and access individual orders using unique IDs. It uses React Router for smooth navigation, Fetch API for backend connection, and CSS for style, including components such as Home, OrderPage, NavBar, NotFoundPage, and OrderDetails.


## Deployment Steps: 

To deploy it, one has to follow these steps after cloning the project.
Deployment steps are: 
After cloning the project, 
1. Installation: Install Docker Desktop.
2. Build the Docker images: Navigate to the root directory of your project in the terminal. Run the command docker-compose up --build. This will initiate the building process for Docker images of your backend servers and MongoDB database.
3. Start the Docker Containers: Docker Compose will automatically launch the Docker containers when the image creation is completed successfully. Your backend servers and MongoDB database are now operational within Docker containers. You can see this both in the terminal and on the Docker desktop. Additionally, make sure to check the status of all containers on a regular basis. Containers may stop working due to firewall settings or random internet access concerns. In such circumstances, just restart the stopped containers from Docker Desktop to restore regular operations.
4. Start the Frontend: After the backend, switch to the frontend directory in your terminal. Execute the command npm install to install the required node modules for the front end. Then, launch the frontend server by running npm run dev.
5. Access the application: Open a web browser and navigate to localhost:3000 (or the port specified for your frontend server, you can see that on the terminal). You should now have access to your sandwich ordering application's user interface.
6. Monitor the Application: Keep an eye on your terminal and Docker Desktop for any error messages or issues during the deployment process. 

By following these deployment steps, one may successfully deploy our sandwich ordering application with Docker for the backend and npm for the front end, granting users access to the program's features.

Application previews
This section includes images of the application's core features and interfaces. These screenshots provide a visual representation of the application's functionality and layout.

Home Page: 
![HomePage](https://github.com/AnisulMahmud/SandwichHub--Sandwich-Ordering-System/assets/52384280/2c3df90e-18d8-4a30-9206-a3c82633746e)

Order List Page: 
![All Order](https://github.com/AnisulMahmud/SandwichHub--Sandwich-Ordering-System/assets/52384280/66ff5c50-5731-490d-8edc-49167ac17430)

Order Details Page: 
![Order Details](https://github.com/AnisulMahmud/SandwichHub--Sandwich-Ordering-System/assets/52384280/e57ccfdf-4cbe-441b-baa1-fecc6dfd91c5)
