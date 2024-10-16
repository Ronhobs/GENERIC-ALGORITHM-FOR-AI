                                              Genetic Algorithm for Optimization in C++

Project Overview
This project implements a simple **Genetic Algorithm** (GA) in C++ to solve an optimization problem. The algorithm seeks to minimize or find a solution to the equation `6*x - y + z^200 = 25` by evolving a population of random solutions through selection, crossover, and mutation. Solutions are ranked based on their fitness, and the algorithm continuously evolves the population to find better solutions.

 How the Algorithm Works
1. **Initial Population:** The algorithm starts by generating a random population of solutions. Each solution is a struct containing three variables (`x`, `y`, and `z`) and a rank (or fitness score).
  
2. **Fitness Function:** The fitness of a solution is determined by how closely it satisfies the equation `6*x - y + z^200 = 25`. Solutions that get closer to solving the equation have a higher rank, while solutions further away have a lower rank.

3. **Selection:** The algorithm selects the top solutions from the current population to form a new "sample" population that will be used for the next generation.

4. **Mutation:** The top solutions are mutated slightly by a small factor (between 0.99 and 1.01) to introduce randomness and explore nearby solutions.

5. **Crossover:** New solutions are generated by combining the mutated solutions. The crossover step randomly selects values from two parent solutions to create a new solution.

6. **Evolution:** This process repeats indefinitely, continuously evolving the population to find better solutions.



How to Run the Project
1. Prerequisites:
Ensure you have a C++ compiler installed (e.g., g++, clang).

2. Compile the Code:
g++ -o genetic_algorithm genetic_algorithm.cpp -std=c++11

3. Run the Program:
./genetic_algorithm
4. Stopping the Algorithm:
The algorithm runs indefinitely in its current form. To stop it, simply terminate the program (e.g., using Ctrl + C).


SAMPLE OUTPUT:
Rank 4532
x: -23.45 y: 67.89 z: 1.25

Rank 3765
x: 12.34 y: -45.67 z: 89.01

...
