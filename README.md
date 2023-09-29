# calculator
a JavaScript implementation of a basic calculator with a graphical user interface (GUI). Here's a description of its main components and functionality:

Variables and Initialization:

runningTotal: A variable to store the running total of the calculations.
buffer: A string variable to hold the current input or calculation buffer.
previousOperator: A variable to store the previously selected arithmetic operator.
screen: A reference to an HTML element with the class name 'screen' for displaying the calculator's input and output.
ButtonClick Function:

This function is called when a button on the calculator is clicked.
It checks whether the clicked button represents a symbol (e.g., '=', 'c', '←') or a number.
Depending on the type of button, it calls either handleSymbol or handleNumber functions.
It updates the screen with the current buffer value.
HandleSymbol Function:

This function handles the logic for symbol buttons (e.g., '=', 'c', '←').
'c': Clears the buffer and resets the running total and previous operator.
'=': Performs a calculation based on the previous operator and updates the buffer and running total.
'←': Deletes the last character from the buffer.
Arithmetic operators ('+', '-', '×', '÷') are also handled here by calling handleMath.
HandleMath Function:

Handles the arithmetic operators ('+', '-', '×', '÷').
Converts the buffer to an integer and performs calculations based on the selected operator.
Updates the running total and sets the current buffer to '0' for further input.
FlushOperation Function:

Performs the actual mathematical operation based on the previous operator.
Updates the running total with the result.
HandleNumber Function:

Appends the selected number to the buffer.
Handles the cases when the buffer is '0' to replace it with the selected number.
Initialization (init) Function:

Initializes the calculator by setting up event listeners for button clicks.
It listens for clicks on elements within the 'calc-buttons' container and calls buttonClick with the clicked button's text.
