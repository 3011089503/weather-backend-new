This project follows a modular structure to ensure scalability and maintainability. 
The configuration layer, implemented in database.ts, manages database connections and environment variables for seamless integration. 
The model layer, defined in Weather.ts, structures the database schema using Sequelize ORM to facilitate interaction with the MySQL database.
Business logic is handled in WeatherService.ts, where API calls to OpenWeatherMap are processed, data is structured, and errors are managed. 
The controller layer, represented by WeatherController.ts, acts as an intermediary between the service and routes, 
handling client requests and formatting responses. API endpoints are defined in WeatherRoutes.ts, 
enabling external access to stored weather data and statistical summaries. 
The job scheduler, implemented in WeatherScheduler.ts, periodically fetches and stores weather data to ensure consistency. 
The application is initiated through server.ts, which sets up the Express server, while app.ts configures middleware and dependencies. 
This structured approach provides a clear separation of concerns, facilitating debugging, testing, 
and future enhancements while ensuring the system remains robust and efficient.

This project uses MySQL as the database to store weather data retrieved from the OpenWeatherMap API. The database is managed using Sequelize ORM, which handles table creation and migrations automatically. The main table, weather_data, stores city names, temperature, humidity, weather descriptions, and timestamps. To set up the database, create a MySQL instance and ensure the correct credentials are provided in the .env file. When the application starts, Sequelize will establish the connection and create the necessary tables if they do not already exist. 

To start, change the .ecv to the  right database URL first. And enter: node dist/server.js
