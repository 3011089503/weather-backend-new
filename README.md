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

To start, change the .ecv to the  right database URL first. And enter: node dist/server.js
