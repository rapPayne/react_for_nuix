# Lab 2: Adding TypeScript

In this lab we'll improve the design of our app by adding TypeScript and then decomposing some components, making them more focused (SRP) and cleaner.


> Beginning with this lab, please always have the RESTful API server running. It is found at [https://github.com/rapPayne/daam-server.git](https://github.com/rapPayne/daam-server.git)

You do not have to populate any data in your app yet. We'll do that in a future lab.

## Creating business classes
Create TypeScript files that export these business classes:
- Film
- Showing
- Theater
- User
- Reservation
To find what properties these should have, make an API call to the server for each.

- You'll also create a class called `Cart` which will have at minimum a list of Seats/Showings. Add to this type as needed in future labs.

## Typing the components
- Edit each component. Specify its type using whichever element type you prefer (FC, ReactElement, etc.)

## Typing the props
- Edit ShowingTimes.tsx. In props, it should receive the filmId and selectedDate. Make sure the props are strongly-typed by adding a type or interface.

Now let's turn to decomposing components ...

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