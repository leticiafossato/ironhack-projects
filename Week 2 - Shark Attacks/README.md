# Week 2 - Shark Attacks

> SHARK ATTACK DATABASE ANALYSIS

> HOW MANY SHARK ACCIDENTS WAS FATAL, NOT FATAL OR UNKNOWN?


## Table of Contents:

> If your `README` has a lot of info, section headers might be nice.

- [Objective](#objectives)
- [Motivation](#motivation)
- [Building](#building)
- [Results](#results)

---

## Objective

- Filter the dataset do discover how many shark accidents was fatal, not fatal or unknown.

### Motivation

- A fear of sharks was implanted in our mind by movies. 
- More people death drown on USA by year than death by shark attacks on the lasts two decades.
- If that sentences above are true, we'll obtain low taxes of deaths.

## Building

1°) Import database, analyse the lenght shape and store a backup;
2°) Clean the lines (drop mean>0.9 of null);
3°) Clean the columns (drop mean>0.9 of null);
4°) Drop CaseNumber2 
5°) Analyse the column 'Fatal (Y/N)':
- Type of data: 
N, Y, UNKNOWN, N, y, N , M, 2017, NaN
- Organizing:
N,N and N -> N
Y and y   -> Y
2017 and M -> UNKNOWN
NaN -> UNKNOWN
6°) Analyse the column 'Issues':
if 'Issues'=Fatal, than:
repace UNKNOWN by Y
7°) Export the database to Excel:
shark_clean_fatal.csv
shark_clean_non_fatal.csv
shark_clean_unknown.csv

## Results 
The quantity of Fatal Accidents is significantly less than Non-Fatal Accidents.
![fatal_graph](https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Fatal.png?raw=true)

Even if we sum the Unknown data do Fatal quantity:
![non_fatal_graph](https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Without_Unknown.png?raw=true)

