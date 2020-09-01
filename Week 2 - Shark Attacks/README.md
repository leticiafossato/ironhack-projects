<p align="center">
  <img width="160" height="140" src="https://imgshare.io/images/2020/09/01/shark_attack.png">
</p>
<h2 align="center">Are most shark accidents fatal or non-fatal?</h>

## Table of Contents:

- [Goal](#goal)
- [Motivation](#motivation)
- [Building](#building)
- [Results](#results)

---

## Goal

- Filter the dataset (source, site= http://www.sharkattackfile.net/whystudy.htm) to discover how many shark accidents was fatal, not fatal or unknown.

### Motivation

- An unreasonable fear of sharks has been implanted in our minds by the hype that surrounds the rare shark attack and by movies. 
- Global Shark Attack File Informs that: more people drown in a single year in the United States than have been killed by sharks throughout the <b>entire world< in the last two centuries</b>. Is that true?

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

<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Week%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Fatal.png?raw=true">

'Fatal (1845 - 2018) Entire World
