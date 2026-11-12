# 📝 Blog REST API

A Blog Management Application built using **Node.js, Express.js, Axios, and EJS**. This project demonstrates RESTful API development and CRUD operations through a two-server architecture, where the frontend communicates with the backend REST API using Axios.

## 🚀 Features

- **Create Posts:** Add new blog posts with title, content, and author.
- **View All Posts:** Retrieve and display all available blog posts.
- **View Single Post:** Fetch a particular blog post using its unique ID.
- **Update Posts:** Partially update existing blog posts using PATCH.
- **Delete Posts:** Remove blog posts using their IDs.
- **RESTful API:** Implement CRUD operations using HTTP methods.
- **Two-Server Architecture:** Separate frontend and REST API servers.
- **Axios Integration:** Connect the frontend with the backend API.
- **Dynamic Rendering:** Display blog posts using EJS templates.
- **Error Handling:** Handle API errors and unavailable posts.

## 🛠️ Tech Stack

- Node.js
- Express.js
- Axios
- Body-Parser
- EJS
- HTML & CSS
- Postman

## 📂 Project Structure

```text
Blog-REST-API/
│
├── node_modules/
├── public/                 # Static files
├── views/                  # EJS templates
│
├── index.js                # REST API server (Port 4000)
├── server.js               # Frontend server (Port 3000)
│
├── package.json
├── package-lock.json
└── README.md
```

## ⚙️ Installation & Setup

**1. Clone the repository**

```bash
git clone <your-repository-url>
```

**2. Navigate to the project directory**

```bash
cd Blog-REST-API
```

**3. Install dependencies**

```bash
npm install
```

## ▶️ Running the Application

The application uses two separate servers. Both must be running simultaneously.

**Step 1: Start the REST API Server**

Open the first terminal:

```bash
node index.js
```

The API server runs at:

`http://localhost:4000`

**Step 2: Start the Frontend Server**

Open a second terminal:

```bash
node server.js
```

The frontend application runs at:

`http://localhost:3000`

Open `http://localhost:3000` in your browser to use the Blog Management Application.

**Important:** Always start the REST API server on port 4000 before starting the frontend server on port 3000.

## 🔗 REST API Endpoints

Base URL: `http://localhost:4000`

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/posts` | Retrieve all blog posts |
| GET | `/posts/:id` | Retrieve a specific post |
| POST | `/posts` | Create a new post |
| PATCH | `/posts/:id` | Update an existing post |
| DELETE | `/posts/:id` | Delete a post |

## 📌 Example API Requests

### 1. Get All Posts

```http
GET http://localhost:4000/posts
```

### 2. Get a Specific Post

```http
GET http://localhost:4000/posts/1
```

### 3. Create a New Post

```http
POST http://localhost:4000/posts
Content-Type: application/json
```

Request Body:

```json
{
  "title": "Learning Node.js",
  "content": "My journey of learning backend development.",
  "author": "Anvi"
}
```

### 4. Update a Post

```http
PATCH http://localhost:4000/posts/1
Content-Type: application/json
```

Request Body:

```json
{
  "title": "Updated Blog Title"
}
```

### 5. Delete a Post

```http
DELETE http://localhost:4000/posts/1
```

## 🔄 Application Workflow

1. The REST API server starts on port 4000.
2. The frontend server starts on port 3000.
3. The frontend uses Axios to send HTTP requests to the REST API.
4. The API processes requests and performs CRUD operations on blog posts.
5. The API sends responses back to the frontend.
6. The frontend renders and displays blog posts using EJS templates.

## 📦 Data Storage

- Blog posts are stored in an in-memory JavaScript array.
- Each post contains an ID, title, content, author, and date.
- New posts receive automatically generated IDs.
- Data resets whenever the REST API server restarts.

## 🎯 Learning Outcomes

- Understanding RESTful API architecture.
- Implementing CRUD operations using Express.js.
- Working with multiple Express servers.
- Connecting frontend and backend using Axios.
- Handling HTTP requests and responses.
- Understanding middleware and routing.
- Rendering dynamic pages using EJS.
- Testing REST APIs using Postman.

## 👩‍💻 Author

**Anvi Mittal**