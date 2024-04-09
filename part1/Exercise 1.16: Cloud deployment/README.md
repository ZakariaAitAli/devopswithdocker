Thank you for the clarification. Deploying a Laravel application to Heroku involves slightly different steps compared to deploying a Java application. Here's how I would approach deploying the "finalLocObjet" Laravel app to Heroku:

## Description
I chose Heroku for cloud deployment due to its simplicity and the availability of a free tier through the GitHub Student Developer Pack. Here are the steps I followed:

1. **Prepare the Application**: Ensured that the "finalLocObjet" Laravel application is containerized using Docker and has a `Dockerfile` configured.

2. **Login to Heroku**: Logged in to my Heroku account using the Heroku CLI.

3. **Create a New Heroku App**: Created a new Heroku app using the `heroku create` command.

4. **Push Docker Image to Heroku Registry**: Used the `heroku container:push` command to push the Docker image to the Heroku Container Registry.

5. **Release the Docker Image**: Released the Docker image to deploy the application using the `heroku container:release` command.

6. **Run Laravel Migrations**: Ran Laravel migrations to set up the database schema on the Heroku dyno.

7. **Access the Running App**: Accessed the running application using the provided Heroku app URL.

## Running App
The "finalLocObjet" Laravel application is now deployed and running on Heroku. You can access it using the following link:
[Link to the Running App](https://your-heroku-app-url.herokuapp.com)

## Dockerfile
Here is the Dockerfile used to containerize the "finalLocObjet" Laravel application:

```Dockerfile
# Use the official PHP image as the base image
FROM php:7.4-fpm

# Set the working directory in the container
WORKDIR /app

# Copy the application files into the container at the specified working directory
COPY . /app

# Install PHP extensions
RUN docker-php-ext-install pdo pdo_mysql

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Install application dependencies
RUN composer install

# Expose port 9000
EXPOSE 9000

# Command to run the application
CMD ["php-fpm"]
```

## Additional Information
- Heroku provides a simple and easy-to-use platform for deploying various types of applications.
- Ensure that the necessary environment variables and configurations are set up in your Heroku application settings.
- For more information on Heroku deployment and configuration, refer to the Heroku documentation.

If you have any questions or need further assistance, feel free to reach out.

Thank you!