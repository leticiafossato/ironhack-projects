<p align="center">
  <img width="160" height="140" src="https://imgshare.io/images/2020/09/01/shark_attack.png">
</p>
<h1 align="center">Week 03</h>
<h2 align="center">Are most shark accidents fatal or non-fatal?</h>

## Table of Contents:

- [Goal](#goal)
- [Motivation](#motivation)
- [Building](#building)
- [Results](#results)
- [Additional](#additional)
- [Improvements](#improvements)
---

## Goal

- Filter the dataset to discover how many shark accidents was fatal, not fatal or unknown.</br>
(Source of database, site= http://www.sharkattackfile.net/whystudy.htm)

### Motivation

- An unreasonable fear of sharks has been implanted in our minds by the hype that surrounds the rare shark attack and by movies. 
- Global Shark Attack File Informs that: more people drown in a single year in the United States than have been killed by sharks throughout the <b>entire world< in the last two centuries</b>. Is that true?

## Building

1°) Import database, analyse the lenght shape and store a backup;<br />
2°) Clean the lines (drop mean>0.9 of null);<br />
3°) Clean the columns (drop mean>0.9 of null);<br />
4°) Drop column CaseNumber2; <br />
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
The quantity of Fatal Accidents is significantly less than Non-Fatal Accidents: </br>

<b>Qty Fatal = 1409 </b></br>
Qty Non-Fatal = 4301  </br>
Qty Unknown = 592 </br>
 </br>
 In percentage:
<b>% Fatal = 0.22357981593145032</br></b>
% Non-Fatal = 0.6824817518248175</br>
% Unknown = 0.09393843224373215</br>
</br>
Using the library matplotlib, we obtain this graph:</br>
<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Fatal.png?raw=true"></br>
This result shows that a low quantity of shaek attacks are fatal, so, the movies that we scared is really difficult to happen.
Also, this database have informations since 1845 to 2018. So, this is the quantity register for more than 173 years. <b>We have less than 8 fatal cases per year at the WORLD.</b></br>
The next graph illustrate that, even if we sum the fatal rate to the unknown rate, the non-fatal still being greater:</br>
<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Without_Unknown.png?raw=true">
</br>
To answer the question made on the beggining (drowns vs fatal shark) I would have another database with these informations. But, I don't have, so I seach for the quantity of drowns on USA per year, and I found the number: 3536 </br>  (source: https://www.cdc.gov/homeandrecreationalsafety/water-safety/waterinjuries-factsheet.html#:~:text=From%202005%2D2014%2C%20there%20were,drowning%20in%20boating%2Drelated%20incidents.&text=About%20one%20in%20five%20people,are%20children%2014%20and%20younger.)</br>
So, the GSAF (Global Shark Attack Files) affirmation was right.
The fatal shark rate from (1845 - 2018) of Entire World is greather than drowns per year at USA.</br>
<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Curiosity.png?raw=true"></br>

## Additional
Using factal attacks, I also analyse the quantity of each type: </br>
provoked - 19</br>
unprovoked- 1182</br>
sea_disaster - 168</br>
boating - 67</br>
boat - 4</br>
questionable- 0</br>
boatomg - 0 </br>
I tried to create a graph with this information, but it doesn't fit.</br>
>> This result highlights that the shark attacks out of curiosity or unintentionally, more than by revenge.</br>

>> The sex with highest fatal rate is male (23,35%) vs female (16,95%). (approximated)

>> The white shark is the specie with more case attacks registered, but it is responsible for only 19 of fatal deaths.

## Improvements
I solved the exercises using mask, but if I restart I would use groupby to clean the solution.