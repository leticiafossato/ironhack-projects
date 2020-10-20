<p align="center">
  <img width="160" height="140" src="https://imgshare.io/images/2020/09/01/shark_attack.png">
</p>
<h1 align="center">🧹 Project 02 | Data Cleaning </h>
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
(Source of database = <a href="http://www.sharkattackfile.net/whystudy.htm">SharkAttackFile</a> )

### Motivation

- An unreasonable fear of sharks has been implanted in our minds by the hype that surrounds the rare shark attack and by movies. 
- Global Shark Attack File Informs: more people drown in a single year in the United States than have been killed by sharks throughout the <b>entire world in the last two centuries </b> . Is that true?

## Building

1°) Import database, analyse the shape,analyse the sample and store a backup;</br>
</br>
2°) Clean the lines (drop mean>0.9 of null);</br>
</br>
3°) Clean the columns (drop mean>0.9 of null);</br>
</br>
4°) Drop column CaseNumber2; </br>
</br>
5°) Analyse the column 'Fatal (Y/N)':</br>
- Type of data: </br>
![type_data](https://i.imgur.com/zATl6Pm.jpg)
</br>
- Organizing:</br>
N,N and N -> N</br>
Y and y   -> Y</br>
2017 and M -> UNKNOWN</br>
NaN -> UNKNOWN</br>
</br>
6°) Analyse the column 'Issues':</br>
if 'Issues'=Fatal and 'Fatal (Y/N)'=UNKNOWN  than:
repace UNKNOWN by Y</br>
</br>
7°) Export the database to Excel:</br>
shark_clean_fatal.csv</br>
shark_clean_non_fatal.csv</br>
shark_clean_unknown.csv</br>
(Check Exported_Files path)

## Results 
The quantity of Fatal Accidents is significantly lower than Non-Fatal Accidents: </br>

<b>Qty Fatal = 1409 </b></br>
Qty Non-Fatal = 4301  </br>
Qty Unknown = 592 </br>
 </br>
 In percentage:</br>
<b>% Fatal = 0.22357981593145032</br></b>
% Non-Fatal = 0.6824817518248175</br>
% Unknown = 0.09393843224373215</br>
</br>
Using the library matplotlib:</br>
<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Fatal.png?raw=true"></br>
> Conclusion: Fatal shark attacks rarely happen.</br>
</br>
Also, this database have informations before 1800 until 2018. Just for analysis, if we consider 1800 as the minimun(it isn't), 1409 is the quantity register for more than 218 years. <b>It means that we have about 7 (= 1409/218) fatal cases per year at the WORLD. Obs: This information is not precise because I don't focus on analyse the 'Year' column.</b></br>
</br>
To make a experience, I sum the Unknown rate to Fatal rate:</br>
<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Without_Unknown.png?raw=true">

> So, even if we sum the fatal rate to unknown rate, the non-fatal still being greater.
</br>
To answer the question made on the beggining (drowns vs fatal shark) I would have another database with these informations. But, I don't have, so I seach for the quantity of drowns on USA per year, and I found the number: 3536 </br>  
(source: <a href="https://www.cdc.gov/homeandrecreationalsafety/water-safety/waterinjuries-factsheet.html#:~:text=From%202005%2D2014%2C%20there%20were,drowning%20in%20boating%2Drelated%20incidents.&text=About%20one%20in%20five%20people,are%20children%2014%20and%20younger.">CDCGov</a>)</br>

<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Project%202%20-%20Shark%20Attacks/Image%20Graphs/Curiosity.png?raw=true"></br>
>So, the GSAF (Global Shark Attack Files) affirmation was right. The fatal shark rate of Entire World is lower than drowns per year on USA.</br>
</br>

## Additional
Using fatal attacks, I also analyse the quantity of each type: </br>
provoked - 19</br>
unprovoked- 1182</br>
sea_disaster - 168</br>
boating - 67</br>
boat - 4</br>

I tried to create a graph with this information, but it doesn't fit.</br>
> This result highlights that the shark attacks out of curiosity or unintentionally, more than by revenge.</br>

> The sex with highest fatal rate is male (23,35%) vs female (16,95%). (approximated)

> The white shark is the specie with more case attacks registered, but it is responsible for only 19 of fatal deaths.

## Improvements
- I answer the questions using mask, but if I restart I would use groupby to solve faster and clear the solution.</br>
- I focus on extract data to answer questions about the database, but the designs of csv file could be cleaned better (some columns with space renamed and data sorted by year).
