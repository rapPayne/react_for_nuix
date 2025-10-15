# Custom Hooks

## Creating an authentication hook
- Create a new file called `useAuth.ts`.
- In this file, export a custom React hook called `useAuth` that manages user authentication state. It should provide methods for logging in, logging out, an isAuthenticated boolean, and a user object.
- Use React's `useState` and `useEffect` hooks to manage and persist authentication state (e.g., using localStorage, zustand, or React context).
- Make sure to type the hook properly using TypeScript.

## Login component
- Create a new component called `Login.tsx`.
- This component should provide a form for users to enter their username and password.
- When the form is submitted, use the `useAuth` hook to log the user in.
- Display appropriate messages for successful login or errors.

## Logging out
- In the `LandingPage` component's nav bar, add a "Logout" button that uses the `useAuth` hook to log the user out when clicked.
- Ensure that the nav bar updates appropriately based on the user's authentication state. 
  - When logged in, show the user's username and a "Logout" button.
  - When not logged in, show "Login" and "Register" buttons. 

## Registering a new user
For this one, you will pull your register logic out of the component and put it into the hook. Consider this step optional but recommended.

- Edit useAuth.ts to include a register method that handles user registration.
- Edit your existing `Register.tsx` component to use the `useAuth` hook for registering new users.
- Ensure that after a successful registration, the user is automatically logged in and redirected to the `LandingPage`.

Note: The login API route returns a JWT. If you want an extra challenge, do something with it like store it in localStorage and use it in the Authorization header for future requests that require authentication.