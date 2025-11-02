**News Explorer API - RESTful Backend Service**

Built a secure, production-ready REST API backend for a news aggregation platform. Implemented JWT authentication, user management, and article CRUD operations with comprehensive security features.

![alt text](https://i.ibb.co/yQwyp0R/123.png "Logo NewsExplorer")

## for the project [news-explorer](http://news-explorer.ru/)

### API Endpoints

- **api.news-explorer.ru**
- **84.201.166.100**

---

### 🧩 Technologies Used

- **Process manager:** pm2
- **HTTP server:** nginx
- **Server:** node.js, express.js
- **SSL certificate:** certbot (Let’s Encrypt)
- **Data validation:** celebrate (Joi)
- **Database:** mongo, mongoose
- **Logging:** winston
- **Others:** npm, git

---

### ⚙️ API Functionality

#### Requests

**GET /users/me**
> Returns user information (email and name)

**GET /articles**
> Returns all articles saved by the user

**POST /articles**
> Creates an article with the following fields in the request body:  
> `keyword`, `title`, `text`, `date`, `source`, `link`, and `image`

**DELETE /articles/:articleId**
> Deletes a saved article by its `_id`

**POST /signup**
> Creates a user with the following fields in the request body:  
> `email`, `password`, and `name`

**POST /signin**
> Verifies the provided email and password and returns a JWT

---

### 🪵 Logging

Logging is configured for:

- **request.log** — stores information about all API requests
- **error.log** — stores information about all errors returned by the API

---

### 🚀 Installation and Launch

**1. Clone the repository**
```bash
git clone https://github.com/zuhijan/news-exlorer-api.git
```



2. Install npm dependencies

> npm install


3. Install MongoDB
> <https://docs.mongodb.com/manual/installation/>

### 🏗️ Run the Project

Production build — start the server on `localhost:3000`

> npm run start


Development build — start the server on `localhost:3000` with hot reload

> npm run dev

### 🔐 Environment Variables (for production)

Create a `.env` file with the following:

> NODE_ENV=production
> JWT_SECRET=some-secret-key
> DB_ADRESS='mongodb://localhost:27017/newsdatab'
