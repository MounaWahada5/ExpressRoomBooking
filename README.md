ExpressRoomBooking API
ExpressRoomBooking is a Node.js backend application for managing reservations. It integrates technologies like Express.js, MongoDB, and robust security practices to offer features such as authentication, data sanitization, advanced queries, and more.

Technologies Used
Node.js: JavaScript runtime.
Express.js: Minimalist web framework.
MongoDB: NoSQL database.
JWT: Secure user authentication.
Mailtrap: Email functionality for development.
Stripe: Payment processing.
Features
Security
Helmet: Secure HTTP headers.
Data Sanitization: Prevent NoSQL injection and XSS.
Rate Limiting: Control excessive requests.
CORS: Enable cross-origin requests.
Content Security Policy (CSP): Block unauthorized scripts.
Query Capabilities
Advanced filtering, sorting, limiting, and pagination via utility class APIFeatures.
Error Handling
Custom error class (AppError) and global error handler middleware.
Authentication
JWT for secure access.
Environment variables for storing sensitive data.
Mailing
Mailtrap for sending booking confirmation emails during development.
Environment Variables

Set up a .env file:
NODE_ENV=development  
PORT=3000  
DATABASE_LOCAL=mongodb://localhost:27017/reservationProject  
JWT_SECRET=your-jwt-secret  
EMAIL_USERNAME=your-mailtrap-username  
EMAIL_PASSWORD=your-mailtrap-password  
STRIPE_SECRET_KEY=your-stripe-key  

API Endpoints
Rooms
GET /api/v1/rooms: Fetch all rooms.
POST /api/v1/rooms: Create a room.
Users
POST /api/v1/users/signup: User signup.
POST /api/v1/users/login: User login.
Reviews
GET /api/v1/reviews: Fetch all reviews.
Reservations
GET /api/v1/reservations: Fetch reservations.
POST /api/v1/reservations: Create a reservation.
Bookings
GET /api/v1/bookings: Fetch bookings.
Security Practices
Environment Variables: Protect secrets like JWT keys and API keys.
Data Sanitization: Prevent harmful scripts or database queries.
Rate Limiting: Block excessive requests.
Content Security: Define policies to block unauthorized external content.
REST API
This project follows REST principles using HTTP methods like GET, POST, PUT, and DELETE for CRUD operations.

