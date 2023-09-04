# StopWatch

HTML Elements:

The code assumes that you have HTML elements in your webpage with specific IDs: stopwatch for displaying the timer, start for the start button, stop for the stop button, and reset for the reset button. These elements are accessed using document.getElementById.
Variables:

timerEl: Holds a reference to the HTML element where the stopwatch time is displayed.
startButtonEl, stopButtonEl, and resetButtonEl: Hold references to the start, stop, and reset buttons, respectively.
Variables for Timing:

startTime: Represents the timestamp when the timer was started or resumed.
elapsedTime: Stores the total elapsed time in milliseconds.
timerInterval: Stores the interval ID for the timer update loop.
startTimer Function:

When the start button is clicked, this function is called.
It calculates the startTime by subtracting the current timestamp from elapsedTime. This allows the timer to resume from where it left off when paused.
It sets up a timer using setInterval that updates the elapsed time and displays it on the page every 10 milliseconds.
It disables the start button and enables the stop button to prevent multiple timer instances from running simultaneously.
formatTime Function:

This function takes the elapsedTime in milliseconds and formats it into a human-readable time format (HH:MM:SS.SS).
It calculates hours, minutes, seconds, and milliseconds from the elapsedTime.
stopTimer Function:

When the stop button is clicked, this function is called.
It clears the timer interval using clearInterval, effectively pausing the timer.
It re-enables the start button and disables the stop button to allow the timer to be started again or reset.
resetTimer Function:

When the reset button is clicked, this function is called.
It clears the timer interval (if running) to stop the timer.
It resets elapsedTime to 0 and updates the timer display to "00:00:00".
It re-enables the start button and disables the stop button.
Event Listeners:

Event listeners are added to the start, stop, and reset buttons to trigger their respective functions when clicked.
