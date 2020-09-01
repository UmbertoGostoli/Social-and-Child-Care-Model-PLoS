# Social-and-Child-Care-Model-PLoS
Social Care Model whose results have been used for the PLoS submission.

The main.py file contains the model's parameters (with the possibility to run the model on multiple threads).
In line 635, the boolean variable 'parametersFromFiles' is set: if False, the values of the parameters will be those indicated in main.py;
if True, the values of the parametrs are read from the csv files 'metaParameters' and 'defaultParameters'.

The main.py file also reads (if 'parametersFromFiles' is set to True) the two csv files 'policyParameters' and 'sensitivityParameters'. In these files, the columns after the first one, contain the name and the values of the parameters we wish to change when simulating different policies or to perform the sensitivity analysis, respectively. The first column contains the 'combinationKey' parameter, which specifies the way the parameters' values will be combined. If 'combinationKey' is set to 1, each row of parameters will be read sequentially; if it is set to 2, the values will be read one at a time (while the others will keep their default value); if it is set to 3, a simulation for each parameters' combination will be run (while if 'combinationKey' is set to 0, no policy or sensitivity run takes place).

The second-to-last column of the 'metaParameters' file contains the 'multiprocessing' parameter: if it is set to True, multiple simulations can be run simultaneously, specifying in the last column the number of processors.

The sim.py file contains the yearly loop and all the functions which are called in each iteration.

The person.py file contains the Person class (with all the indivdiual variables) and the Population class, which is the collection of persons
(which is created at the beginning of the simulation and updated each year.

The house.py file contains the House class (with the variables associated with each house), the Town class (with the list of houses of each town)
and the Map class (with the list of towns).

The version of Python is Python 2.7.14 and the following packages are needed: numpy 1.14.0, pandas 0.22.0 and networkx 2.1

To run the model, in the Anaconda prompt go to the folder when the files have been downloaded, digit 'python main.py' and press Enter.

When starting the simulation, a folder called 'Simulations_Folder' will be automatically created in the same folder of the files. Here, the simulation's results are saved (in the Outputs.csv file).



