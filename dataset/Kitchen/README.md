DATASET DESCRIPTION

The dataset contains the samples collected as part of the "Kitchen Cleaning Experiment" described in paper:

Davide, Bacciu; Maurizio, Di Rocco; Mauro, Dragone; Claudio, Gallicchio; Alessio, Micheli; Alessandro, Saffiotti, "An Ambient Intelligence Approach for Learning in Smart Robotic Environments" Computational Intelligence, 2019

The "./Data" folder contains 80 csv files, one for each sample in the dataset.

Each sample file kitchen$i.csv (where $i is the sample number) contains a comma separated list of 27 input features plus the associated target, that are:
* The reading of the light, PIR, temperature and humidity transducers of the 6 WSN motes deployed in the experiment, for a total of 24 features.
* The position of the robot during the execution of the task expressed as 2D position (X,Y) plus orientation (THETA).
* The target associated to the execution of the task as assessed by the Performance Monitor component, that is a value in {0,1} where 0 failure in the execution of the cleaning task, while 1 succesful conclusion of the cleaning task. 

DATASET FORMAT

File kitchen$i.csv contains information on the execution of the i-th Kitchen Cleaning task.

A row contains the 27 input features plus the target output organized as the following orderd list of comma-separated values (LIGHT1 denotes the reading of the light transducer on mote 1, LIGHT2 on mote 2, etc.):
 
LIGHT1, PIR1, TEMP1, HUMID1, LIGHT2, PIR2, TEMP2, HUMID2, LIGHT3, PIR3, TEMP3, HUMID3, LIGHT4, PIR4, TEMP4, HUMID4, LIGHT5, PIR5, TEMP5, HUMID5, LIGHT6, PIR6, TEMP6, HUMID6, X, Y, THETA, TARGET

Each row denotes a time-step of the sequence, where measurements are sampled at 2Hz. 
