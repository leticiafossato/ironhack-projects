<p align="center">
  <a href="https://imgbb.com/"><img src="https://i.ibb.co/SDSjQV1/shark5.jpg" alt="shark5" border="0"></a>
</p>
<h1 align="center">🧹 Project 02 | Data Cleaning </h>

## Project Status
:heavy_check_mark: Complete

## Table of Contents:

- [Goal](#goal)
- [Motivation](#motivation)
- [Process](#process)
- [Results](#results)
- [Learning Process](#learning-process)
- [Author](#Author)

## Goal

- Apply different cleaning and manipulation techniques to generate a cleaner CSV version of the dataset
<a href="http://www.sharkattackfile.net/whystudy.htm">SharkAttackFile</a>.<br>
To acess complete goal informations click <a href="https://drive.google.com/file/d/1t1-Ud2PbfCXpNpQX7bjy66saUXqjsmsa/view?usp=sharing">here</a>.
### Business question
> Are most shark accidents fatal or non-fatal?

### Motivation

- An unreasonable fear of sharks has been implanted in our minds by the hype that surrounds the rare shark attack and by movies. 
- Global Shark Attack File Informs: more people drown in a single year in the United States than have been killed by sharks throughout the <b>entire world in the last two centuries </b> . Is that true?

## Process
1. Import database, analyse the shape,analyse the sample and store a backup;<br>
2. Clean the lines (drop if NaN mean>0.9);<br>
3. Clean the columns (drop if NaN mean>0.9);<br>
4. Drop column CaseNumber2; <br>
5. Analyse the column 'Fatal (Y/N)':<br>
    - Type of data: <br>
    
    |  Data       |     Quantity     |  
    | ----------  | -----------------|  
    |N            |      4293        |   
    |Y            |      1388        | 
    |UNKNOWN      |       71         | 
    |&nbsp;N      |       7          | 
    |N&nbsp;      |       1          | 
    |M            |       1          | 
    |2017         |       1          | 
    |y            |       1          | 
    
    <a href="https://i.imgur.com/zATl6Pm.jpg">+ Details</a>

    - Organizing:<br>

    |   Original             |    Transform    |  
    | ----------             | ----------------| 
    |N,&nbsp;N, N&nbsp;      |      N          |   
    |Y, y                    |      Y          | 
    |UNKNOWN, M, 2017, NaN   |    UNKNOWN      | 

6. Analyse the column 'Issues':<br>
if 'Issues'=Fatal and 'Fatal (Y/N)'=UNKNOWN  than:
replace UNKNOWN by Y<<br>
7. Export the database to Excel (Exported_Files path):<br>
shark_clean_fatal.csv<br>
shark_clean_non_fatal.csv<br>
shark_clean_unknown.csv<br>

## Results 
The quantity of Fatal Accidents is significantly lower than Non-Fatal Accidents: </br>
| Qty Fatal  |    Qty Non-Fatal    |   Qty Unknown   |
| ---------- | -----------------   |  ---------------|
|   1409     |       4301          |      592        |  
 </br>
 In percentage:
 
| % Fatal    |    % Non-Fatal    |     % Unknown   |
| ---------- | ----------------- |  ---------------|
|  0.2235    |       0.6825      |      0.09394    |  

</br>
Using the library matplotlib:</br>
<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Project%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Fatal.png?raw=true"><br>

> Conclusion: Fatal shark attacks rarely happen.</br>

</br>
Also, this database have informations before 1800 until 2018. Just for analysis, if we consider 1800 as the minimun(it isn't), 1409 is the quantity register for more than 218 years. <b>It means that we have about 7 (= 1409/218) fatal cases per year at the WORLD. Obs: This information is not precise because I don't focus on analyse the 'Year' column.</b></br>
</br>
To make a experience, I sum the Unknown rate to Fatal rate:</br>
<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Project%202%20-%20Shark%20Attacks/Image%20Graphs/Results_Quantity_Without_Unknown.png?raw=true">

> So, even if we sum the fatal rate to unknown rate, the non-fatal still being greater.
</br>
To answer the question made on the beggining (drowns vs fatal shark) I would have another database with these informations. But, I don't have, so I seach for the quantity of drowns on USA per year, and I found the number: 3536 </br>  
(source: <a href="https://www.cdc.gov/homeandrecreationalsafety/water-safety/waterinjuries-factsheet.html#:~:text=From%202005%2D2014%2C%20there%20were,drowning%20in%20boating%2Drelated%20incidents.&text=About%20one%20in%20five%20people,are%20children%2014%20and%20younger.">CDCGov</a>)</br>

<img align="center" src="https://github.com/leticiafossato/ironhack-projects/blob/master/Project%202%20-%20Shark%20Attacks/Image%20Graphs/Curiosity.png?raw=true"></br>
>So, the GSAF (Global Shark Attack Files) affirmation was right. The fatal shark rate of Entire World is lower than drowns per year on USA.</br>

### Additional
Using fatal attacks, I also analyse the quantity of each type: </br>

| Type         |    Qty   |  
| ----------   | ---------|
| provoked     |   19     |    
| unprovoked   |   19     |  
| sea_disaster |  168     | 
| boating      | 67       | 
| boat         | 4        | 

> This result highlights that the shark attacks out of curiosity or unintentionally, more than by revenge.</br>

> The sex with highest fatal rate is male (23,35%) vs female (16,95%). (approximated)

> The white shark is the specie with more case attacks registered, but it is only responsible for 19 of fatal deaths.

## Learning Process
### Challenges
- Understand the dataset;
- Choose which columns explore;
- Organize the column Fatal (Y/N);

### New Learnings
- Display information visually (matplotlib).

### Theory Applied
- [x]  Pandas (Import and Export data)<br>
- [x] Explore Analysis Data<br>
- [x] Data Manipulation (Filtering)<br>
- [x] Data Cleaning <br>

### Improvements
- I answer the questions using mask, but if I restart I would use groupby to solve faster and clear the solution.</br>
- I focus on extract data to answer questions about the database, but the designs of csv file could be cleaned better (some columns with space renamed and data sorted by year).

## Author
Letícia Fossato
