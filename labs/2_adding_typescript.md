# Lab 2: Adding TypeScript

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

