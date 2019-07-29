DATASET DESCRIPTION

The dataset contains the samples collected as part of the "Entrance Mirror Experiment" described in paper:

Davide, Bacciu; Maurizio, Di Rocco; Mauro, Dragone; Claudio, Gallicchio; Alessio, Micheli; Alessandro, Saffiotti, "An Ambient Intelligence Approach for Learning in Smart Robotic Environments" Computational Intelligence, 2019

The folder contains 65 csv files, one for each sample in the dataset, partitioned in 2 subfolders:
*"./dataCurved" Contains samples related to curved navigation trajectories which are those where the laser-based navigation quality is influenced by the presence of the mirror.
*"./dataStraight" Contains samples related to stright navigation trajectories where the impact of mirror presence is negligible.

Each sample file mirror$i.csv (where $i is the sample number) contains a comma separated list of 27 input features plus the associated target, that are:
* The reading of the light, PIR, temperature and humidity transducers of the 6 WSN motes deployed in the experiment, for a total of 24 features.
* The position of the robot during the execution of the task expressed as 2D position (X,Y) plus orientation (THETA).
* The target associated to the execution of the task as assessed by the Performance Monitor component, that is a value in [0,1] where 0 denotes totally unsatisfactory performance, while 1 denotes maximum performance. 

DATASET FORMAT

File mirror$i.csv contains information on the execution of the i-th Entrance navigation task.

A row contains the 27 input features plus the target output organized as the following orderd list of comma-separated values (LIGHT1 denotes the reading of the light transducer on mote 1, LIGHT2 on mote 2, etc.):
 
LIGHT1, PIR1, TEMP1, HUMID1, LIGHT2, PIR2, TEMP2, HUMID2, LIGHT3, PIR3, TEMP3, HUMID3, LIGHT4, PIR4, TEMP4, HUMID4, LIGHT5, PIR5, TEMP5, HUMID5, LIGHT6, PIR6, TEMP6, HUMID6, X, Y, THETA, TARGET

Each row denotes a time-step of the sequence, where measurements are sampled at 2Hz. 

