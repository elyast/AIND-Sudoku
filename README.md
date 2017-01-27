# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: In order to find naked twins I iterated over units (column, row, etc) and first pick the box values that are of size 2.
In order to find actual twins I build reverse dictionary to find boxes with identical values 
(dictionary maps box value -> set of box keys, e.g. '23':{}, '45':{'A1', 'A2'})
Next we need to remove those duplicated values (digit by digit) from boxes in the same unit other than the boxes we found (naked twins).


# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: I noticed that diagonal sudoku problem really adds 2 more units, 2 diagonals to be exact to the unit list.
I generated those using list comprehension, and added them to unitlist.
Rest of the solution works in the same way there is no change to the code.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.
