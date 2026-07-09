# Blogify

A full-stack application built with the MERN stack (MongoDB, Express, React, Node.js).

## Tech Stack

**Backend** (from `package.json`)
- Express
- Mongoose
- jsonwebtoken
- bcrypt
- cloudinary
- multer
- cors
- dotenv
- nodemon (dev dependency)

**Frontend** (from `package.json`)
- React
- React Router (react-router-dom)
- Axios
- Tailwind CSS
- Vite
- ESLint (dev dependency)

## Backend Setup (from `index.js`)

- Express app with JSON and URL-encoded body parsing enabled
- CORS enabled
- Connects to MongoDB via Mongoose using a `MONGO_URL` environment variable
- Loads environment variables via `dotenv`
- Listens on a `PORT` environment variable, defaulting to `3000`

### Routes mounted

- `/user` → `./routes/user`
- `/blog` → `./routes/blog`
- `/comments` → `./routes/comments`

(The contents of these route files were not reviewed, so their specific endpoints/behavior aren't documented here.)

## Scripts

**Backend**

| Script | Command |
|---|---|
| `npm run dev` | `nodemon index.js` |
| `npm start` | `node index.js` |

**Frontend**

| Script | Command |
|---|---|
| `npm run dev` | `vite` |
| `npm run build` | `vite build` |
| `npm run lint` | `eslint . --ext js,jsx --report-unused-disable-directives --max-warnings 0` |
| `npm run preview` | `vite preview` |

## Getting Started

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/blogify.git
   cd blogify
   ```

2. Install backend dependencies
   ```bash
   npm install
   ```

3. Install frontend dependencies
   ```bash
   cd client
   npm install
   ```

4. Set the following environment variables for the backend (required by `index.js`):
   ```env
   MONGO_URL=your_mongodb_connection_string
   PORT=3000
   ```

   (Additional environment variables may be required by the route files, e.g. for `jsonwebtoken` or `cloudinary`, but these were not confirmed in the reviewed code.)

## License

ISC (as declared in `package.json`).
