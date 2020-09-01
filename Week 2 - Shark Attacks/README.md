<p align="justify">![img](https://imgshare.io/images/2020/09/01/shark_attack.png)
## SHARK ATTACK DATABASE ANALYSIS</center></p>
>> Are most shark accidents fatal or non-fatal?</center> 


## Table of Contents:

- [Goal](#goal)
- [Motivation](#motivation)
- [Building](#building)
- [Results](#results)

---

## Goal

- Filter the dataset do discover how many shark accidents was fatal, not fatal or unknown.

### Motivation

- A fear of sharks was implanted in our mind by movies. 
- More people death drown on USA per year than death by shark attacks on last two decades.
- If that sentences above are true, we'll obtain low taxes of deaths.

## Building

1°) Import database, analyse the lenght shape and store a backup;<br />
2°) Clean the lines (drop mean>0.9 of null);<br />
3°) Clean the columns (drop mean>0.9 of null);<br />
4°) Drop CaseNumber2; <br />
5°) Analyse the column 'Fatal (Y/N)':<br />
- Type of data: <br />
![type_data](https://i.imgur.com/zATl6Pm.jpg)
<br />
- Organizing:<br />
N,N and N -> N<br />
Y and y   -> Y<br />
2017 and M -> UNKNOWN<br />
NaN -> UNKNOWN<br />
6°) Analyse the column 'Issues':<br />
if 'Issues'=Fatal, than:
repace UNKNOWN by Y<br />
7°) Export the database to Excel:<br />
shark_clean_fatal.csv
shark_clean_non_fatal.csv
shark_clean_unknown.csv

## Results 
The quantity of Fatal Accidents is significantly less than Non-Fatal Accidents:
![fatal_graph](https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Fatal.png?raw=true)
Even if we sum the Unknown data do Fatal quantity:
![non_fatal_graph](https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Without_Unknown.png?raw=true)


model_graph_source = https://matplotlib.org/3.3.1/gallery/pie_and_polar_charts/pie_features.html#sphx-glr-gallery-pie-and-polar-charts-pie-features-py


'Fatal (1845 - 2018) Entire World
