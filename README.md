## Tic Tac Toe

## Purpose of Project

The purpose of this project is to refamiliarize myself with a quick React refresher. This will be my starting point in getting back into React and an opportunity to improve my documentation skills. Wish me luck!

## Quick Overview

This is a Tic-Tac-Toe [tutorial](https://reactjs.org/tutorial/tutorial.html) from reactjs.org to create a React web application.

There are 2 phases for this project:
1) Creating a fully functional tic-tac-toe game
2) Adding a "time machine" feature that will allow users to revert back to a previous turn

## Technical Overview

This application has 3 components, square (a function component), Board, and Game.

The Game component includes the state of the application that includes data relevant to the history of moves made, who's turn it is next, and the current move number. This state is manipulated when a user clicks on a square on the board or on the "Go to move n" / "Go to game start" buttons. These buttons are binded to methods on this component.

Two methods, handleClick and jumpTo are included on the Game component. The handleClick method updates the state's history, checks to see if there's a winner, and updates which player is next. This method is used by the Board component and Square component and is passed down through props. The jumpTo method will revert the game to the state of the game of the corresponding move number of the button clicked. It will also revert to the corresponding user's turn.

The board component renders the 9 squares with the values 0 to 8. These values are matched to check if there's a winner. Each square is rendered passing in values to the renderSquare method. This method returns an instance of the Square component.

The Square component returns a button with the value passed in from the Board component.

It is important to note that values and the handleClick method is passed down from parent to child components. For example:

Game's handleClick() == Board's onClick == Square's onClick

## How to run this application?
1) Ensure you have node.js installed
2) Ensure you have Git installed
3) Clone this repo
4) run `npm start` in the command line in the cloned directory

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Contact

Feel free to contact me for any discrepancies of information, questions or concerns via [Linked In](https://www.linkedin.com/in/kevin-ma-9145a8110) or [email](mailto:kevin@kevin-ma.com). I am always open to construct criticism!
