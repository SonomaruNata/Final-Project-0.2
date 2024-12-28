# final-project-2024

Project for my friends : an innovative e-commerce platform designed for fashion lovers who value sustainability and creativity. The site empowers users to create unique, stylish looks by mixing and matching second-hand items with handmade products. Our goal is to reduce fashion waste by giving pre-loved pieces a second life, while supporting artisans and small businesses. With a curated collection of vintage, upcycled, and bespoke fashion, Julia raskin StyleOn brings together community, creativity, and conscious consumerism.


## Overview
Final-Project-2024 is a full-stack web application developed as part of a final project for W310523ER. The project utilizes modern web technologies including **React.js** for the frontend, **Node.js** for the backend, and **MongoDB** as the database. The application implements user authentication, protected routes, and an admin dashboard for managing products and orders.

## Technologies Used
- **Frontend:** React.js, React Router, Axios
- **Backend:** Node.js, Express.js
- **Database:** MongoDB, Mongoose
- **Authentication:** JSON Web Tokens (JWT)
- **Styling:** Bootstrap, Custom CSS
- **Version Control:** Git, GitHub

## Features
- User Authentication (Sign-up, Sign-in, JWT-based authorization)
- Admin Dashboard for managing users, products, and orders
- Responsive design with Bootstrap
- Product browsing and shopping cart functionality
- Protected routes for admin and user areas

## Setup and Installation
### Prerequisites
- Node.js (v20.14.0 or higher)
- MongoDB (installed and running locally or cloud instance)
- Git

### Installation
1. Clone the repository:
```bash
   git clone https://github.com/SonomaruNata/Final-Project-WEB.git
```
2. Navigate to the project directory:
```bash
   cd Final-Project-WEB
```
3. Install dependencies for both client and server:
```bash
   cd client
   npm install
   cd ../server
   npm install
```

### Configuration
1. Create a `.env` file in the server directory with the following:
```
JWT_SECRET=your_jwt_secret
MONGO_URI=mongodb://localhost:27017/finalprojectdb
PORT=5000
```
2. Update the `axiosInstance.js` file in the client directory to match your backend URL:
```javascript
const axiosInstance = axios.create({
  baseURL: 'http://localhost:5000',
});
export default axiosInstance;
```

### Run the Application
1. Start the backend server:
```bash
   cd server
   nodemon server.js
```
2. Start the frontend:
```bash
   cd client
   npm start
```

### Access the Application
- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:5000`

## Project Structure
```
Final-Project-WEB/
│
├── client/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── assets/
│   │   └── axiosInstance.js
│   └── package.json
│
├── server/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middlewares/
│   └── server.js
│
├── .env
├── package.json
└── README.md
```

## API Routes
### Public Routes
- `POST /api/users/login` - User login
- `POST /api/users/register` - User registration

### Protected Routes
- `GET /api/users/profile` - Fetch user profile (requires JWT)
- `GET /api/admin/users` - Admin fetches user list
- `DELETE /api/admin/users/:id` - Admin deletes a user

## Deployment
1. Build the frontend for production:
```bash
   cd client
   npm run build
```
2. Deploy to a platform like Heroku, Vercel, or Netlify.

## Contributing
Contributions are welcome! If you'd like to improve the project:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/new-feature`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Create a Pull Request.

## License
This project is licensed under the MIT License.



