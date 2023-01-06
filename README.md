# Genetic-Algorithm-From-Scratch
A GA (Genetic Algorithm) optimized Peak Function in Python

Population
Population intializes by generating randomly.
In my case, for continuous variables(x,y), both limited value in the range [-5, 5].

Fitness Calculation
Each chromosome from the population is passed to the objective function one by one and its fitness is calculated.

Crossover
Task to produce new solutions from existing solutions 
First I determine the pool size and then choose the best chromosomes based on the pool size  (i.e. parents are chosen from this mating pool 
to perform crossover in the next phase)
Two individual parents produce through mating selection (i.e one-point crossover,multipoint crossover, uniform crossover)  to produce offspring.

Mutation
Typically, childern inherit 99% of characteristics from their parents but mutation allows to introduce new traits.
It maitain diviersity and stop population converging at premature stage.
I implement random initialization mutation (FYI:Flip mutation,Swap mutation, Random initialization)

Survivors’ selection
This stage decide who will survive for the next generation/iteration. (FYI:Random selection, Proportionate selection, Merging parents and new offspring)
The survival of good solutions will lead the algorithm to converge while it may cause the algorithm to converge prematurely. 
Hence, some poor solutions should be given chance to survive, which will allow GA to maintain diversity and enhance exploration

How to terminate the algorithm?
(1)A predefined number of iterations are completed.
(2)A predefined fitness value is obtained.
(3)There is no improvement in results for a fixed number of iterations.
