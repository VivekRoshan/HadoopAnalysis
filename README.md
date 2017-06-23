# HadoopAnalysis

In this assignment, we work on hadoop analysis on a datafile containing 900,000 and 29 columns. <br>
The code is written in such a way that, only the words in the columns from 25 to 29 are printed out as the the standard output for the reducer.<br>
The mapper accepts the standard input from the datafile /data/nyc/nyc-traffic.csv. <br>
The final output would be the unique words and its counter that is passes through mapper and reducer. <br>

**Steps to execute**<br>
1. Clone the project: git clone https://github.uc.edu/suggalvn/HadoopAnalysis <br>
2. Run the command on hadoop server: <br>
   *hadoop jar /opt/hadoop-2.7.1/share/hadoop/tools/lib/hadoop-streaming-2.7.1.jar -file /home/suggalvn/mapper.py    -mapper /home/suggalvn/mapper.py -file /home/suggalvn/reducer.py   -reducer /home/suggalvn/reducer.py -input /data/nyc/nyc-traffic.csv  -output /user/suggalvn/homeworkoutput* <br>
3. Now view the results from the path */user/suggalvn/homeworkoutput* : <br>
   *hadoop fs -cat /user/suggalvn/homeworkoutput/**

**Outputs Obtained**
*Statistics Summary results:*<br>

[suggalvn@cscloud2017 ~]$ hadoop fs -cat /user/suggalvn/homeworkoutput/* <br>
AMBULANCE       3713 <br>
BICYCLE 24153 <br>
BUS     25871 <br>
FIRE TRUCK      1333 <br>
LARGE COM VEH(6 OR MORE TIRES)  27981 <br>
LIVERY VEHICLE  17775 <br>
MOTORCYCLE      10029 <br>
OTHER   51360 <br>
PASSENGER VEHICLE       1005161 <br>
PEDICAB 123 <br>
PICK-UP TRUCK   26281 <br>
SCOOTER 534 <br>
SMALL COM VEH(4 TIRES)  30048 <br>
SPORT UTILITY / STATION WAGON   363210 <br>
TAXI    63892 <br>
UNKNOWN 105481 <br>
VAN     51666 <br>

    
