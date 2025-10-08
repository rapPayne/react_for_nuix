# Lab 4: Adding routing

In this lab we'll decompose some components, making them more focused (SRP) and therefore better designed. Then we'll add routing so that we can navigate from component to component seamlessly.

## Decomposing DatePicker
That `<section>` where you're displaying the days of the week -- that should be broken into its own component called DatePicker. 
- Create DatePicker.tsx
- In it, display the days of the week as you did before.
- When the user selects a day, set the showing date selected by the user into the global data store (hint: use Zustand)
- Note that when done right, this should cause the ShowingTimes instances to re-render because they use the selected date. Make sure you test this.

## Decomposing FilmBrief
Again on `<LandingPage />`, notice that you're showing essentially the same thing six times but each with a different film.
- Decompose that section into a new component called FilmBrief.tsx.
- This should receive a Film object as props. Make sure they're strongly typed.

Now let's turn to routing...

Feel free to look back at the chapter notes or look online for the low-level instructions on how to set up routing.

## Install routing
- Using npm, install TanStack Router.
- Edit vite.config.ts, registering the router compiler.

## Setting up routing
- Edit main.tsx to be aware of the router
- Add the folders and files needed for the baseline routing (hint: __root.tsx, index.tsx)
- Move the page-level components into the routes folder. (hint: For easier debugging, do this one-by-one and test each rather than moving them all in.)

## Using `<Link>`
- Edit LandingPage.tsx. The film briefs should be links to /films/:filmId where :filmId is the actual ID of the film.
- Edit ShowingTimes.tsx. The showing times should be links to /pick-seats/:showingId where :showingId is the actual ID of the showing.

## Route parameters
- Film details should be at "/films/:filmId". Make sure that the FilmDetails component reads the filmId from the route parameters and fetches the film details accordingly.
- PickSeats should be at "/pick-seats/:showingId". Make sure that the PickSeats component reads the showingId from the route parameters and fetches the showing details accordingly.

## Pushing to a route
When the user clicks "Check out" in PickSeats, we need to push to the /checkout route.
- Edit the button's onClick handler to push to /checkout using the router's navigation mechanism