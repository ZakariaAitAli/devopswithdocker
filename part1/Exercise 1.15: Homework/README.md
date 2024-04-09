# Exercise 1.15: Homework

Dockerized Project - Gestion de Temps de Travail

## Overview
For Exercise 1.15, I have containerized the backend of the "Gestion de Temps de Travail" project, which is a Java EE web application. This README provides instructions on how to run the containerized backend using Docker.

## Project Description
"Gestion de Temps de Travail" is a web application for managing employee work time within a company. The backend, hosted in the [GestionTempsTravail](https://github.com/ZakariaAitAli/GestionTempsTravail) repository, is developed using Java EE. The frontend, hosted in the [GTT](https://github.com/ZakariaAitAli/GTT) repository, is developed using Next.js and deployed on Vercel.

## Docker Hub Link
The Docker image for the backend of the "Gestion de Temps de Travail" project is available on Docker Hub at the following link:
[Image ZakariaAitAli/Gestion_Temps_Travail](https://hub.docker.com/r/zakariaaitali/gestion_temps_travail)

## Instructions
Follow these steps to run the backend of the "Gestion de Temps de Travail" application using Docker:

1. **Clone the Backend Project**:
   ```
   git clone https://github.com/ZakariaAitAli/GestionTempsTravail.git
   ```

2. **Navigate to the Project Directory**:
   ```
   cd GestionTempsTravail
   ```

3. **Start MySQL Server**:
   ```
   docker-compose up -d
   ```

4. **Create the Database**:
   ```
   docker exec -i mysql mysql -uroot -psecret < ./database.sql
   ```

5. **Run the Java Server**:
   ```
   mvn spring-boot:run
   ```

6. **Access the Application**:
   Open your web browser and go to:
   ```
   http://localhost:3000
   ```

## Additional Information
- Make sure you have Docker, Docker Compose, Git, Maven, Java 21, and MySQL installed before running the application.
- For the frontend part of the application developed in Next.js, refer to the [GTT](https://github.com/ZakariaAitAli/GTT) repository.
- For more information on the backend project, including setup instructions and usage guidelines, refer to the original project repository: [Gestion de Temps de Travail Backend](https://github.com/ZakariaAitAli/GestionTempsTravail).
  
If you encounter any issues or have questions, feel free to reach out.

Thank you!