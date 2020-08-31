# Social-and-Child-Care-Model-PLoS
Social Care Model whose results have been used for the PLoS submission.

The main.py file contains the model's parameters (with the possibility to run the model on multiple threads).

The sim.py file contains the yearly loop and all the functions which are called in each iteration.

The person.py file contains the Person class (with all the indivdiual variables) and the Population class, which is the collection of persons
(which is created at the beginning of the simualtion and updated each year.

The house.py file contains the House class (with the variables associated with each house), the Town class (with the list of houses of each town)
and the Map class (with the list of towns).

The version of Python is Python 2.7.14 and the following packages are needed: numpy 1.14.0, pandas 0.22.0 and networkx 2.1

