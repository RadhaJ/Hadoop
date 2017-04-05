# Cloud-Assignment-4
Utilize Hadoop for Dataset Analysis


In this project Hadoop streaming API is used to build mapper and reducer scripts that analyze the dataset stored in cluster. 

Run the following commands in order to run the program:

1)Clone the program from github URL 
git clone https://github.uc.edu/jarubura/Cloud-Assignment-4

2)Run the below command in order to retrieve the log:

hadoop jar /opt/hadoop-2.7.1/share/hadoop/tools/lib/hadoop-streaming-2.7.1.jar -file /home/jarubura/mapper.py    -mapper /home/jarubura/mapper.py -file /home/jarubura/reducer.py   -reducer /home/jarubura/reducer.py -input /data/nyc/nyc-traffic.csv  -output /user/jarubura/hw4

3)Run the following program to see the output:

hadoop fs -cat /user/jarubura/hw4/*

OUTPUT OBTAINED:
AMBULANCE       3713
BICYCLE 24153
BUS     25871
FIRE TRUCK      1333
LARGE COM VEH(6 OR MORE TIRES)  27981
LIVERY VEHICLE  17775
MOTORCYCLE      10029
OTHER   51360
PASSENGER VEHICLE       1005161
PEDICAB 123
PICK-UP TRUCK   26281
SCOOTER 534
SMALL COM VEH(4 TIRES)  30048
SPORT UTILITY / STATION WAGON   363210
TAXI    63892
UNKNOWN 105481
VAN     51666

This dataset has more than million records of collision incidents each involving 5 types of vehicles. This Mapper code fetches columns with vehicles in key,value pair and sends them into reducer which calculates summary counts of each vehicles.

With this homework I understood the basic concept of MapReduce Paradigm and could solve this simple summary count problem.
