# React + Vite

React Router CRUD Application Documentation
Live Demo: https://react-router-crud.vercel.app/

Overview
This React application implements a simple CRUD (Create, Read, Update, Delete) functionality for managing employee data. It uses:

React functional components and hooks (useState, useEffect).

React Router v6 for client-side routing.

Bootstrap 5 for styling.

LocalStorage for data persistence.

The app allows users to:

Add new employee records.

View a list of employees.

Edit existing employee records.

Delete employees from the list.

Application Structure
bash
Copy
Edit
/src
  /components
    Employee.jsx         # Form for adding/editing employee
    EmployeeData.jsx     # Table displaying employee list with edit/delete
    Header.jsx           # Optional header/navigation (if included)
  App.jsx                # Main app component managing state and routing
  main.jsx               # Entry point with ReactDOM and BrowserRouter
Key Features
1. Routing
/ — Shows the Employee form for adding or editing employee data.

/view — Displays the EmployeeData table with all employees.

React Router’s Routes and Route components handle navigation seamlessly with useNavigate.

2. Employee Form (Employee.jsx)
Controlled inputs for Name, Post, and Salary.

onChange prop handles input updates.

onSubmit prop handles form submission for both add and update modes.

Button text changes dynamically based on whether the form is adding a new employee or editing an existing one.

3. Employee Table (EmployeeData.jsx)
Displays employees in a responsive Bootstrap table.

Shows Edit and Delete buttons for each row.

Edit button loads employee data into the form for updating.

Delete button removes the employee from the list.

4. State Management (App.jsx)
Employee data is managed using React's useState.

On app load, employee data is retrieved from localStorage to persist data across page refreshes.

On any CRUD operation, localStorage is updated to keep data in sync.

editId tracks which employee is being edited.

Navigation handled via React Router’s useNavigate.

How to Use
Add Employee

Visit / (default route).

Fill in the employee name, post, and salary.

Click Add Data to save.

You will be redirected to /view.

View Employees

Visit /view.

See a list of all employees.

Click Edit to modify an employee or Delete to remove.

Edit Employee

On /view, click Edit next to an employee.

You are redirected back to / with pre-filled data.

Modify details and click Update Data.

Redirects back to /view.

Installation & Running Locally
bash
Copy
Edit
git clone https://github.com/your-repo/react-router-crud.git
cd react-router-crud
npm install
npm start
Dependencies
react

react-dom

react-router-dom

bootstrap

Live Demo
Access the live app here: https://react-router-crud.vercel.app/