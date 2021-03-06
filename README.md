# N-puzzle
N-puzzle solver using A* algorithm with a visualizer of the generated solution.
This solver works for any puzzle size although 4-puzzles and up can take a lot of time to be completed.

![](resources/visualizer.gif)

> This is what the visualizer looks like. Note that the empty space of the puzzle is not represented.

> You can press R to pause/play and left/right arrow keys to navigate move by move.
# Required packages
* Numpy
* Matplotlib
* Pygame

# Usage
If you launch the n-puzzle program without arguments you will get the solving of a 3-puzzle that has been scrambled with 100 random moves. 
By default, the used heuristic function will be the Manhattan distance however, you can change a lot of parameters thanks to the implemented options:
```
$> python n-puzzle.py -h
usage: n-puzzle.py [-h] [-m file] [-vi] [-vb] [-g size] [-i number]
                   [-gr | -un] [-t]
                   [-hf {Manhattan,Euclidian,Tiles out-of-place}]

optional arguments:
  -h, --help            show this help message and exit
  -m file, --map file
  -vi, --visu           Enable visualization
  -vb, --verbose        Enable verbose (may slow the algorithm down)
  -g size, --generate size
                        Generate a n-size puzzle
  -i number, --iteration number
                        Choose the number of scrambling moves
  -gr, --greedy         Enable greedy search
  -un, --uniform        Enable uniform-cost search
  -t, --time            Print the algorithm's execution time
  -hf {Manhattan,Euclidian,Tiles out-of-place}, --heuristic {Manhattan,Euclidian,Tiles out-of-place}
                        Heuristic function choice, (default: Manhattan)
```
If you want to solve your own puzzle, be sure to follow the same format as in resources/grid.txt (the first number is the size of the puzzle).
Note that the defined solved state for this program is in shape of a spiral with 0 representing the empty space.
So for example a 3-puzzle's solved state is:
```
1 2 3
8 0 4
7 6 5
```
# Credit
This project was made by:
* Julien Dumay (https://github.com/ChokMania), main tasks: argument parsing and visualizer
* myself, Aleksi Gautier (https://github.com/Kelias-42), main tasks: grid generation and solving algorithm
