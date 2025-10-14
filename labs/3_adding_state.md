# Lab 3: Adding state

Up to this point, our components are filled with hardcoded data. In this lab, we'll be adding state to the components we created in Lab 1 and typed in Lab 2. We'll fetch data from the server and write it to state, both locally with useState and globally with Zustand.

For all of the data fetching, handle errors gracefully. At minimum, log the error to the console and display a user-friendly message in the UI. You can either show a toast notification or un-hide a <div> that contains the message. Bonus points for showing a loading indicator while the data is being fetched.

## Fetching films
- In the landing page component, use useEffect to call the server and fetch the list of films when the component first loads. Store that list in state. Then render the list of films from state.
- Put these films in a global store with Zustand so that other components can access them as needed.

## Fetching showings
- In ShowingTimes, the component that displays showings for a selected day, use useEffect to fetch the showings for that film and that day from the server. Store the showings in local state and render them.
- Think about whether you want to also store these in the global Zustand store. What are the pros and cons of doing so? Can you think of any problems with that approach? Can you think of any benefits?

## Using Zustand for global state
- Create a Zustand store to hold global state such as the user's cart and selected seats. Update the components to read from and write to this global state as needed.