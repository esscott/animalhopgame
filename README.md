# animalhopgame
Animal Hop Game for CSC 111 Final Project at Smith College
Programmers Emma Scott & Molly Swope

## REQUIRED FILES
- finalproject.py
- graphics.py
- scoreboard.py
- rabbit.py
- squirrel.py
- skunk.py

## EXPLANATION OF HOW TO RUN PROJECT
1. Download required files
2. Be sure required files are in the same location
3. Open finalproject.py in Python Idle
4. Run finalproject.py module
5. Enter user name
6. Enter yes/no to view/not view scoreboard
7. Enter bunny, squirrel, or skunk to choose animal
8. Window titled “Animal Hop Game” appears
9. Click anywhere on that window to begin game
10. Press any key to jump and avoid obstacles
11. If you hit an obstacle, you will have two more chances before the game is over

## PROJECT DESCRIPTION
- The primary objective/purpose of the Animal Hop Game is to entertain young children with an interactive game that allows them to make choices between different animal avatars and to self-set and meet goals by keeping track of high scores
- The intended audience is young children whose parents are looking for a simple, non-violent computer game to entertain them while they do projects around the house, run errands, or make phone calls

## ARCHITECTURE DESCRIPTION
Animal() class: 
- Constructor takes in name, window, position, and choice attributes
- Methods include draw and jump
- Purpose is to draw the chosen animal’s image to the window and allow it to move up and down vertically in a jumping motion with user keyboard taps

Obstacle() class:
- Constructor takes in window, position, and two points
- Methods include draw, move, and get top left
- Purpose is to draw randomly colored, rectangular obstacles to window and move them across horizontally, to the left

Background() class:
- Constructor takes in window
- Includes draw method
- Purpose is to draw a background to the window with a green rectangle as the ground and a blue rectangle as the sky

findScore() function:
- Purpose is to open scoreboard.py file, append name and respective time scores separated by spaces and new lines, and close file

storeScores() function:
- Purpose is to open scoreboard.py file, read it, create a dictionary for the scores and names, sort scores from highest to lowest, display top five scores, and to use a try/except block is included to allow for program to run before five scores are recorded

main() function:
- Purpose is to display opening greeting, prompts, and instructions to shell, call classes and functions, display warning messages to window, and keep track of score using time library

## MAJOR CHALLENGE DISCUSSION
We faced a major challenge early on. When working towards a minimum viable project, we got hung up on the issue of making obstacles move across the screen continuously and randomly as we were only able to figure out how to make one obstacle come and go. In order to overcome it, we went to the next available TA Hours and the TA suggested that meet our goal, we would have to type a new code block for every obstacle that we wanted to appear. This was somewhat disheartening, so we then went to get a second opinion at office hours where we learned that there was a relatively simple way to make a kind of conveyor belt looping pattern where boxes would exit the screen on the left and reenter the screen on the right at random times. The next night, we were able to implement this fix, and we were off and running once again. 
