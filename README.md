
---

# FitMi

A full-stack FitMi Tracking App built with the MERN (MongoDB, Express, React, Node.js) stack. This app allows users to log and track daily health metrics such as body temperature, blood pressure (systolic/diastolic), and heart rate. Users can create, view, update, and delete health records, while also utilizing features like searching and filtering through the records.

## Features

- **Authentication API Features:**
    The Authentication API now includes a registration feature with an improved UI, allowing users to input detailed personal information.

    - User Registration:
    The registration form allows new users to sign up by providing the following details:
    Name: The user's full name.
    Email: A valid email address for account setup.
    Password: A secure password for account login.
    Gender: Gender selection (Male/Female/Other).
    Height (cm): The user's height in centimeters.
    Weight (kg): The user's weight in kilograms.
    These details are stored securely in the backend database and can be used to personalize health recommendations and metrics tracking in future updates

- **Dashboard:**
  - Displays a list of all health records with metrics such as body temperature, blood pressure, and heart rate.
  - Records that exceed reference values are highlighted in red, and records below the reference are highlighted in yellow also the records that fit perfectly in the given reference range those are highlighted in green.
  - Smooth UI transitions and animations using Framer Motion and Tailwind CSS.
  
- **Add New Record:**
  - Users can add new health records with the following fields:
    - Date
    - Body temperature (in °F)
    - Blood pressure (Systolic/Diastolic)
    - Heart rate (in bpm)
  - Upon adding a new record, the dashboard is updated instantly.

- **View & Update Record:**
  - View an existing health record via a modal that pops up without navigating away from the page.
  - Users can modify the health record directly in the modal, with pre-filled data for convenience.
  - Updated values are highlighted with visible effects and animations to indicate changes.

- **Delete Record:**
  - Users can delete any health record from the dashboard.

- **Search & Sort Records:**
  - Search functionality allows users to filter health records based on specific metrics (date, body temperature, blood pressure, heart rate).
  - Sort records in ascending or descending order by any health metric.
  
- **Responsive Design:**
  - Mobile-friendly UI with a dark, stylish theme using Tailwind CSS.

## Tech Stack

### Frontend:
- **React.js**: For building the user interface.
- **Framer Motion**: For smooth animations and transitions.
- **Tailwind CSS**: For custom styling and a modern, responsive layout.

### Backend:
- **Node.js** & **Express.js**: For handling API requests and routing.
- **MongoDB**: As the database to store user health records.
- **Mongoose**: For MongoDB object modeling.
- **CORS**: Middleware to handle cross-origin requests.
- **Google API**: For user authentication via Gmail.

### API Endpoints:
  ## Authentication API: 
  - **POST /api/register**: Register a new user.
  - **POST /api/login**: Log in a user.
  - **PUT /api/users/:id**: Update user information.
  ## Health Records 
  - **GET /api/health-records/:userId**:Retrieve a list of health records for a specific user.
  - **POST /api/health-records/:userId**: Create a new health record for a specific user.
  - **GET /api/health-records/:userId/:id**: Retrieve a health record by ID for a specific user.
  - **PUT /api/health-records/:userId/:id**: Update a health record by ID for a specific user.
  - **DELETE /api/health-records/:userId/:id**: Delete a health record by ID for a specific user.

## Getting Started

### Prerequisites

- **Node.js** (v14 or above)
- **MongoDB** (local or cloud instance)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/vinodkata/FitMi.git
cd FitMi
```

2. Install dependencies for both the frontend and backend:

```bash
# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install
```

3. Create a `.env` file in the `server` folder with the following contents:

```bash
MONGO_URI=<your-mongodb-connection-string>
PORT=5000
```

4. Start the server and client:

```bash
# Start the server (backend)
cd server
npm start

# Start the client (frontend)
cd ../client
npm run dev
```

The app should now be running on:
- Frontend: `http://localhost:5173`
- Backend: `http://localhost:5000`

### Deployment

To deploy the app, you'll need to deploy both the frontend and backend. You can use platforms like [Render](https://render.com/) or [Vercel](https://vercel.com/).

1. **Frontend**: Deploy the React app to Vercel or any static hosting service.
2. **Backend**: Deploy the Node.js API to Render, Heroku, or any Node.js hosting provider.

Make sure to update the frontend API URL in `client/src/services/api.js` to match the deployed backend URL.

## Future Enhancements

- **Graphical Representation**: Add charts and graphs to visualize health data trends over time.
- **Export Data**: Provide users with the ability to export their health records to CSV or PDF formats.

## License

This project is licensed under the MIT License - see the [LICENSE](client/LICENSE) file for details.

---
