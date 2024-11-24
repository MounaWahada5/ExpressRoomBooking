"ExpressRoomBooking API
This project is a comprehensive Node.js backend application designed for managing reservations. It leverages a variety of technologies including Express.js, MongoDB, and various security practices to provide a robust solution for booking management. It offers features such as user authentication, data sanitization, advanced query capabilities, and much more.

*Technologies Used
Node.js: JavaScript runtime built on Chrome's V8 JavaScript engine.
Express.js: A fast, unopinionated, minimalist web framework for Node.js.
MongoDB: A NoSQL database for storing data.
JWT (JSON Web Tokens): Used for secure user authentication.
Mailtrap: Used for email functionality during development.
Stripe: Integrated for payment processing.
Features
1. Security
Helmet: Provides secure HTTP headers to protect from web vulnerabilities.
Data Sanitization: Protects against NoSQL injection and XSS attacks using tools like express-mongo-sanitize and xss-clean.
Rate Limiting: Prevents abuse from excessive requests using express-rate-limit.
CORS: Allows cross-origin requests to enable secure resource sharing across different domains.
Content Security Policy (CSP): Prevents unwanted scripts from running in the browser.
2. Query Features
Advanced Filtering, Sorting, Limiting, and Pagination: The project includes a utility class (APIFeatures) to handle complex query operations for enhanced data retrieval.
3. Error Handling
Centralized Error Handling: Custom error class (AppError) to handle errors globally.
Global Error Handler Middleware: Catches and processes errors across the application to send proper error responses.
4. Authentication
JWT Authentication: Ensures secure login and access to routes.
Environment Variables: For secure storage of sensitive information such as JWT secrets and database credentials.
5. Mailing
Mailtrap: Used for sending emails (e.g., booking confirmations) during development.
Environment Variables
Make sure to create a .env file and chang it :

env
Copy code
NODE_ENV=development
PORT=3000
USER=med
PASSWORD=0000
DATABASE_LOCAL=mongodb://localhost:27017/reservationProject
JWT_SECRET=azer-rtyu_uioopi1qsdf02hghjjhk3kklkl4cxcvw6dfqdf@
JWT_EXPIRES_IN=90d
JWT_COOKIES_EXPIRES_IN=90
EMAIL_USERNAME=66026a0857bf21
EMAIL_PASSWORD=6219501413751d
EMAIL_HOST=sandbox.smtp.mailtrap.io
EMAIL_PORT=25
EMAIL_FROM=hello@hmm.com
STRIPE_SECRET_KEY=sk_test_51P3VG3EIAjF2DWAzkrOuZBT7SYIje8VhFyiUSwtCDWLhFfgrRSwhNcgi8Dhy2n7hDAx8qIG1sPRfSTQmDUeljAxC009lq2PU4Z


API Endpoints
1. Rooms
GET /api/v1/rooms - Fetch all rooms.
POST /api/v1/rooms - Create a new room.
2. Users
POST /api/v1/users/signup - User signup.
POST /api/v1/users/login - User login.
3. Reviews
GET /api/v1/reviews - Fetch all reviews.
4. Reservations
GET /api/v1/reservations - Fetch reservations.
POST /api/v1/reservations - Create a reservation.
5. Bookings
GET /api/v1/bookings - Fetch bookings.
Security Practices
Environment Variables: Protect sensitive information by storing secrets like JWT keys, database URIs, and API keys in environment variables.
Data Sanitization: Ensure that all user inputs are sanitized to prevent malicious scripts or harmful database queries.
Rate Limiting: Prevent denial-of-service (DoS) attacks by limiting the number of requests from a single IP.
Content Security: Define policies to block unauthorized external content and mitigate security risks.
REST API
This project follows REST (Representational State Transfer) principles, using standard HTTP methods like GET, POST, PUT, and DELETE for CRUD operations. Routes are organized in RESTful patterns, where each resource (e.g.,  rooms, users) has its own dedicated endpoint, making it easy to interact with the system programmatically."
