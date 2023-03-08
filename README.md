
# React Router
This project is a sample web application built using React and React Router. It includes several pages and layouts, such as a home page, about page, and careers page, as well as error handling and authentication functionality. The application fetches data from a local API to display information about available careers. The code is organized into separate components, and the routing is handled by the React Router library.

## App.js
- This code sets up the client-side routing for a React application using the "react-router-dom" package. It defines a router using the "createBrowserRouter" function and sets up routes using the "createRoutesFromElements" function, which takes a tree of React elements and converts them into an array of routes.

The routes include:

- A route for the home page ("/") that uses a "RootLayout" component and displays a "Home" component as its index page.
A route for the "about" page ("/about") that displays an "About" component.
- A route for the "help" section ("/help") that uses a "HelpLayout" component and contains two sub-routes for the "faq" and "contact" pages.
- A route for the "careers" section ("/careers") that uses a "CareersLayout" component and contains two sub-routes, one for the list of careers and another for the details of a single career. The "loader" props are used to fetch data for the careers and career details pages.
- A catch-all route that displays a "NotFound" component for any undefined routes.
- The "App" component sets up the routing context by wrapping the "RouterProvider" around the router. Overall, this code sets up the basic structure for a client-side routed React application.
## Careers Component
- This code exports a React component Careers which renders a list of careers loaded from the careersLoader function. The useLoaderData hook is used to access the data returned by the careersLoader function. The component renders a link to each career page which is represented by its ID in the URL path.

- The careersLoader function fetches a list of careers from a JSON API endpoint and returns the parsed JSON data. If the request is unsuccessful, it throws an error with a message.
## About Component
- This is a functional React component called About that imports useState and Navigate from the react-router-dom library.

- The component renders a div that contains a heading, three paragraphs, and a button. The component also has a state isLogin which is set to true by default. If isLogin is true, the component renders the div with the content and the button. If isLogin is false, the component redirects to the homepage using the Navigate component.

- The component can be used in a route by importing and including it in the routes.

### Contact Component

- This code defines a React component called "Contact", which displays a contact form and handles its submission. It imports the "Form", "redirect", and "useActionData" functions from the "react-router-dom" package.

- When the user submits the form, the "contactAction" function is called, which extracts the email and message from the form data, checks if the message length is greater than 10 characters, and returns an error if it is not. If there are no errors, the function returns a redirect to the home page.

- The "Contact" component uses the "useActionData" hook to display any error messages returned by the "contactAction" function. The component displays a form with an email input and a message textarea, and a submit button. When the user clicks the submit button, the form data is sent to the server using a POST request.


