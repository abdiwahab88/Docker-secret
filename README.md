# Docker-secret
Docker secrets provide a secure and convenient way to manage sensitive information, such as database credentials, within a Dockerized application.
To implement that, we Deploy WordPress and MySQL using Docker Compose with Docker secrets, here are the steps:

-	Create a **docker-compose.yml** file in your project directory.
-	Define the WordPress and MySQL services within the **docker-compose.yml** file, specifying the necessary configuration such as image versions, ports, and environment variables.
-	Create two secret files in your project directory: **db_password.txt** and **db_root_password.txt**, containing the WordPress database password and MySQL database root password, respectively by using **docker secret create** command.
-	Configure the WordPress service to use Docker secrets by specifying the secrets in the **secrets** section of the service definition. Use the **file** attribute to reference the corresponding secret files.
-	Configure the MySQL service to use Docker secrets in a similar manner, referencing the appropriate secret files for the WordPress database password and MySQL root password.
-	Open a terminal, navigate to your project directory, and execute the **docker-compose up** command.

<p>Executing these steps will initiate the deployment of WordPress and MySQL containers, with the Docker secrets securely injected into the services.</p>



