Routine-X: A Simple Todo Application
A straightforward and user-friendly to-do list application built to demonstrate a full-stack web development workflow, from initial setup to deployment.

View Live Demo on Render (https://routine-x.onrender.com)

The "Why" Behind the Tech
This project was more than just building another to-do app, it was an exercise in making deliberate technology choices and understanding the trade-offs, just like in a real engineering team. 

Here’s a breakdown of my thought process;

Frontend: React + Vite
React: I chose React because its component-based structure is great for building UIs that are easy to manage. Breaking down the app into smaller pieces like TodoList, TodoItem, and an input form made the code cleaner
and more reusable. It's a practical approach that scales well.
Vite: For the development environment, I picked Vite over the older Create React App because of its speed. Vite's Hot Module Replacement (HMR) is incredibly fast, which meant I could see changes in the browser 
almost instantly without waiting for a full rebuild. This saved a lot of time during development.

Backend: Node.js + Express
Node.js & Express: Using JavaScript on both the frontend and backend just made sense. It allowed me to stay in the same language context, which is more efficient. Express is a minimalist framework for Node.js that 
provides just enough structure for building a robust API without being overly complex. It was perfect for creating the simple REST API this app needed (e.g., GET /api/todos, POST /api/todos).

Database: MongoDB
MongoDB: I went with a NoSQL database like MongoDB because of its flexibility. When you're building a new application, requirements can change. MongoDB's document-based structure (using Mongoose as the object modeling tool)
let me store data in a JSON-like format, which maps directly to the JavaScript objects used in my app. This made it simple to work with the data without being locked into a rigid schema from the start.

API Communication: Axios
On the frontend, I used Axios to talk to the backend API. While the native fetch API is perfectly fine, Axios has a simpler, promise-based syntax that I find cleaner for handling HTTP requests and responses. It also 
automatically handles transforming JSON data, which is a small but nice convenience.

Deployment: Render
I deployed this project on Render because it offers a straightforward experience for full-stack applications. It has a free tier and can automatically deploy new changes whenever I push code to the main branch on GitHub.
This setup creates a simple continuous deployment pipeline, demonstrating an important industry practice without extra complexity.

How to Run This Project Locally:

Clone the repository:
git clone https://github.com/Timani723/routine-x
cd routine-x

Install Backend Dependencies:
# From the root directory
npm install

Install Frontend Dependencies:
cd frontend
npm install

Set up Environment Variables: Create a .env file in the backend directory and add your MongoDB connection string
MONGO_URI=your_mongodb_connection_string

Run the Application:
Start the Backend Server: In the root directory, run:

npm start
The server will run on http://localhost:5000.

Start the Frontend Development Server: In a new terminal, navigate to the frontend directory and run:

npm run dev
The app will be available at http://localhost:5173.
