# React Job Board

This project is a job board application built with React that allows users to view, add, edit, and delete job listings. The jobs are fetched from a backend API created using `json-server`, simulating a real backend.

## Features

- **View Job Listings**: Users can view all job listings from the backend API.
- **Add Job**: Users can add a new job to the job board.
- **Edit Job**: Users can edit existing job details.
- **Delete Job**: Users can delete a job listing.
- **View Job Details**: Each job listing can be viewed individually for more detailed information.

## Project Structure

```plaintext
react-job-board/
│
├── public/                 # Public folder for static assets
├── src/                    # Main source folder for the project
│   ├── components/         # Reusable components (JobList, JobDetail, JobForm, etc.)
│   ├── pages/              # Pages for routing (Home, JobDetailPage, etc.)
│   ├── services/           # API services for fetching job data from json-server
│   ├── App.js              # Main app component
│   └── index.js            # Entry point for React
│
├── db.json                 # JSON file for json-server database
├── package.json            # Project dependencies and scripts
└── README.md               # Project documentation
```

## How It Works

#### Frontend

The frontend of the job board is built using React. It interacts with the backend API for job-related operations, utilizing React's state and lifecycle methods for fetching and managing data.

#### Backend

The backend is simulated using json-server, which provides a simple and easy-to-use REST API. The jobs.json file acts as the database for job listings, storing job data

## Available Scripts

In the project directory, you can run:

#### Install dependencies

```plaintext
npm install
```

#### Start the json-server backend (port 5000)

```plaintext
npx json-server --watch db.json --port 5000
```

#### Start the frontend React app (port 3000)

```plaintext
npm start
```

The app will run at http://localhost:3000, and the json-server backend will run at http://localhost:5000.

## API Endpoints

The backend API exposes the following endpoints:

- GET /jobs: Fetch all job listings.
- GET /jobs/:id: Fetch a single job listing by ID.
- POST /jobs: Add a new job listing.
- PUT /jobs/:id: Update an existing job listing.
- DELETE /jobs/:id: Delete a job listing by ID.

## Features in Detail

1. Fetching Jobs: The job listings are fetched from the API using the fetch method or Axios, and displayed in the UI. A JobList component maps over the fetched jobs and displays them in a list format.

2. Adding a Job: Users can add a job using a form component (JobForm). The form allows input for job details like title, company, and description. On form submission, a POST request is made to the API to add the job.

3. Editing a Job: Existing job listings can be edited using the same form. When the "Edit" button is clicked on a job listing, the form is pre-filled with the job’s details, and a PUT request is sent to the API to update the job.

4. Deleting a Job: A job can be deleted by clicking the "Delete" button next to the job listing. This sends a DELETE request to the API, removing the job from the backend.

5. Viewing Job Details: Clicking on a job listing shows the full details of the job on a separate page. This is handled by React Router, using dynamic routing to fetch and display the job based on its ID.

## Dependencies

- React: Frontend framework for building the UI.
- json-server: Provides a simple mock API for CRUD operations.
- Axios: For making HTTP requests to the API.
- React Router: Handles client-side routing for navigating between job listings and details.
- React Hooks: Used for managing state and effects within components.

## Setup and Installation

1. Clone this repository to your local machine.

```plaintext
git clone https://github.com/akshatpandey1903/react-job-board.git
cd react-job-board
```

2. Install the necessary dependencies:

```plaintext
npm install
```

3. Start the json-server:

```plaintext
npx json-server --watch jobs.json --port 5000
```

4. Start the React application:

```plaintext
npm run start
```

The React app will automatically open in your browser at http://localhost:3000.

## Future Enhancements

- Search functionality: Add a search bar to filter job listings.
- Pagination: Implement pagination for job listings to improve performance.
- Authentication: Add user authentication to allow users to manage their job listings.
- Advanced Validation: Add form validation for job creation and editing.
