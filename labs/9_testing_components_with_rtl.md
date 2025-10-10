# Testing Components with React Testing Library

## Setting up React Testing Library
- Install React Testing Library and its dependencies.
- Configure your testing environment to work with React Testing Library.
- Run a smoke test to ensure that the setup is correct.

## Showing Times Component
Your showing times component now uses a function to fetch its data. You also exercised mocking that function in your tests.

- Write a test for the showing times component that verifies it renders correctly with mock data.
- Ensure that the test checks for the presence of key elements in the component, such as the proper showing times.

## Seat Selection Component
At this point you have a component where the seat map will eventually go. Let's populate it with some seats using TDD.
- Write a test for the seat selection component that verifies it renders.
- Write a test that verifies that the component renders the movie title, showing time, and theater name.
- Write a test that verifies that the component renders a check out button.

These tests may pass without any effort on your part depending on what you implemented in the previous labs. But the rest won't (unless you got ambitious and worked ahead.)

- Write a test that verifies that X tables rendered.
- Make that test pass.
- Modify that test or create a new one that verifies that the tables have numbers on them.
- Make that test pass.

## Draw some seats
- Write a test that verifies that Y seats rendered.
- Make that test pass.
- Write a test that verifies that the seats have numbers on them.
- Make that test pass.
- Write a test that verifies that a given table has the proper number of seats rendered.
- Make that test pass.

You can't pick seats that are already taken so ...

- Write a test that verifies that seats that are already reserved are rendered differently (e.g., with a different class name).
- Make that test pass.

![the seat selection component](/assets/PickSeats.png)