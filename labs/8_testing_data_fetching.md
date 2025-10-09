# Testing Data Fetching

Now that we're experts with testing synchronous code, let's explore how to test asynchronous code, specifically around data fetching.

## Putting showing times fetch under test
- Refactor your showing times fetch logic into a repo function called "fetchShowingTimes".
- Write a test for fetchShowingTimes. Note that if you don't mock it, it will make a real API data request, which is slow and brittle. Go ahead and try it if you want.
- Now, mock the API request. You can use `vi.fn()` or `vi.mock()`. You can use `vi.spyOn()` if you are clever about how you implement it.
- Get a running test.
- Bonus: Test error handling.

## Testing the other fetches
Try out using TDD techniques to implement and test the other fetches in your app. 
- Test fetching films.
- Test fetching a single film.
- Test fetching theaters.