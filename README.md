# Bubble-click-Game
a fun game where you need to click on a bubble based on the number shown in the target within a specific time.


Sure, here's a summary of the complete code.

### GameBoard Component (GameBoard.jsx):

- The `GameBoard` component manages the main functionality of the bubble clicking game.
- It imports the `Hit`, `Timer`, `Points`, and `Bubble` components.
- The component starts with initial values for time, bubbles, points, game over status, and target.
- Inside the component, a function `generateRandomNumber` generates a random number between 1 and 10.
- It uses `useState` to manage remaining time, bubbles, points, game over status, and target state.
- In the `useEffect` hook, bubbles are initialized with random numbers.
- The component handles bubble clicks with `handleBubbleClick`, which increases points and generates a new target number if the clicked bubble's number matches the target.
- Another `useEffect` hook manages the countdown timer, sets game over status when time reaches 0, and clears the interval when the component unmounts.
- The return section renders the game's UI, including the hit target, timer, and bubbles.

### Hit Component (Hit.jsx):

- The `Hit` component displays the current target number that the player should click on.
- It receives the `target` prop indicating the current target number to display.
- The component uses `React.memo` to optimize rendering when the target number doesn't change.
- The UI displays the target number in a rounded box.

### Timer Component (Timer.jsx):

- The `Timer` component displays the remaining time for the game.
- It receives the `remainingTime` prop indicating the time left in seconds.
- Similar to the `Hit` component, `React.memo` optimizes rendering when the remaining time doesn't change.
- The UI displays the remaining time in a rounded box.

### Points Component (Points.jsx):

- The `Points` component displays the player's current score.
- It receives the `points` prop indicating the player's score.
- `React.memo` is used to optimize rendering when the score doesn't change.
- The UI displays the score in a rounded box.

### Bubble Component (Bubble.jsx):

- The `Bubble` component represents each clickable bubble in the game.
- It receives the `number` prop representing the number on the bubble and the `onClick` prop to handle bubble clicks.
- The `handleClick` function is defined to pass the clicked bubble's number to the `onClick` handler.
- When a bubble is clicked, the `onClick` handler in the `GameBoard` component is invoked.

Overall, the components work together to create a bubble clicking game where players need to click bubbles with numbers that match the target number displayed. The game also features a timer, point tracking, and a game over state. The code demonstrates the usage of state management, effects, prop passing, and `React.memo` to optimize rendering.
