<h1>Tic-Tac-Toe Game React18</h1>
This is a simple tic-tac-toe game built using React from React.dev Documentation.

<h3>Getting Started</h3>
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

<h4>Prerequisites</h4>
You need to have Node.js and npm installed on your machine.

<h4>Installing</h4>
<ul>
<li>Clone the repository</li>
 <li>Navigate to the project directory in your terminal</li>
 <li>Run "npm install" to install the dependencies</li>
 <li>Run "npm start" to start the development server</li>
 <li>Open http://localhost:3000 to view it in the browser</li>
</ul>

<h3>Game Rules</h3>
<ul>
<li>The game is played on a 3x3 grid</li>
  <li>Players take turns placing their respective mark (X or O) on an empty square.</li>
  <li>The first player to get three of their marks in a row (horizontally, vertically, or diagonally) wins the game.</li>
  <li>If all squares are filled and no player has won, the game is a draw.</li>
</ul>


<h3>Code Structure</h3>
<h4>"Square" Component</h4>
This component renders a button with the value passed as a prop. When the button is clicked, it calls the "onSquareClick" function passed as a prop.

<h4>"Board" Component</h4>
This component renders the 3x3 grid of squares. It receives the current state of the game (an array of 9 values, either "X", "O", or null) as a prop, along with a boolean value indicating which player's turn it is. It also receives a callback function onPlay to be called when a square is clicked.

When a square is clicked, handleClick function is called. It checks if the clicked square is already filled or if a player has already won. If either of those conditions is true, it returns early. Otherwise, it updates the game state by updating the nextSquares array and calling onPlay with the updated state.

The component also checks if there is a winner using the calculateWinner function. If there is a winner, it displays the winner. Otherwise, it displays which player's turn it is.

<h4>"Game" Component</h4>
This component is the top-level component of the game. It maintains the game history in the history state variable, where each element of the array is an array representing the state of the game at that move. It also maintains the currentMove state variable, which represents the index of the current move.

When a move is made, the handlePlay function is called, which updates the history state variable and the currentMove state variable.

The component also renders a list of buttons, one for each move in the game history. When a button is clicked, it calls the jumpTo function with the index of the move to jump to.

<h4>"calculateWinner" Function</h4>
This function takes an array representing the state of the game and checks if there is a winner. It does this by checking all possible winning combinations of squares.


<h2>Enjoy The Game!</h2>
