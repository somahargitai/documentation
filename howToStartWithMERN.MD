# Start a MERN stack project with Unity game

## install node, npm, nvm

_node package manager, node version manager_

(https://nodejs.org/en/download/package-manager)[https://nodejs.org/en/download/package-manager]

## Frontend

create a react app with create-react-app, which sets up

```bash
npx create-react-app frontend
cd frontend
```

## Backend

```bash
mkdir backend
cd backend
npm init -y
npm install express mongoose dotenv cors
```

create an index.js file in the backend folder

```javascript
const express = require('express');
const mongoose = require('mongoose');
const cors = require('cors');
const dotenv = require('dotenv');

dotenv.config();

const app = express();
app.use(cors());
app.use(express.json());

app.get('/', (req, res) => {
  res.send('API is running');
});

const PORT = process.env.PORT || 5000;
app.listen(PORT, () => {
  console.log(`Server is running on port ${PORT}`);
});
```
