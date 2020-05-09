Question 2
-------------------
Consider a table storing temperature readings taken by sensors: 
```SQL
   Temps(sensorID, time, temp)
```
Assume the pair of attributes [sensorID,time] is a key. Consider the following query: 
```SQL
   select * from Temps
   where sensorID = 'sensor541'
   and time = '11:15:06'
```
Consider the following scenarios:
* A - No index is present on any attribute of Temps
* B - An index is present on attribute sensorID only
* C - An index is present on attribute time only
* D - Separate indexes are present on attributes sensorID and time
* E - A multi-attribute index is present on (sensorID,time)

Suppose table Temps has 70 unique sensorIDs and each sensorID has exactly 30 readings. Furthermore there are exactly 20 readings for every unique time in Temps.

For each scenario A-E, determine the maximum number of tuples that might be accessed to answer the query, assuming one "best" index is used whenever possible. (Don't count the number of index accesses.) Which of the following combinations of values is correct? 
