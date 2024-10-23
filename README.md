Snake Game using Python (Pygame, Tkinter & MySQL)
Table of Contents
Introduction
Features
Requirements
Installation
How to Run the Game
Database Setup
Game Features
Screenshots
Contributing
License
Introduction
This is a Python implementation of the classic Snake game using the Pygame library for gameplay, Tkinter for the GUI, and MySQL for storing high scores and player information. Players can play the game, view top scores, delete records, and visualize scores using graphs.

Features
Play the Snake game in various difficulty levels.
View and store player scores in a MySQL database.
Display the top 10 highest scores.
Delete player records.
Visualize the player's scores over time with a graph.
Requirements
Python 3.x
Pygame
Tkinter
Matplotlib
MySQL Connector (pymysql)
Installation
Step 1: Clone the Repository
bash
Copy code
git clone https://github.com/yourusername/snake-game-python.git
cd snake-game-python
Step 2: Install Dependencies
You will need to install Python and the necessary libraries:

bash
Copy code
pip install pygame pymysql matplotlib
Step 3: Set Up MySQL
Ensure you have MySQL installed on your system. You will need to create a user and database for this project.

Step 4: Configure MySQL Credentials
In the Python code, adjust the MySQL connection details:

python
Copy code
mycon = sqlcon.connect(
    host="localhost", 
    user="root",  # Change to your MySQL username
    database="game_stats", 
    passwd="root",  # Change to your MySQL password
    charset='utf8'
)
How to Run the Game
After installing the dependencies and setting up the MySQL database, run the snake_game.py file:

bash
Copy code
python snake_game.py
You will see a GUI window where you can enter the player name and age to start the game.

Once the game ends, the score is automatically saved in the MySQL database.

Database Setup
The game will automatically create the required database (Game_Stats) and table (Game_Stats) if they don't exist.

The Game_Stats table stores:

Name: The player's name.
Age: The player's age.
Score: The player's score.
You can manage the database (view, delete, and insert records) via the Tkinter interface.

Game Features
Snake Movement: Use the arrow keys to control the snake's movement.
Scoring: The snake's score increases as it eats food.
Game Over: The game ends if the snake collides with the boundary or itself.
High Scores: View the top 10 high scores and delete records directly from the GUI.
Graphical Representation: Visualize the player's scores across different matches using a graph.
