<p align="center"><h1 align="center">Week 04</h></p>
<h2 align="center">:arrow_forward: Data Gathering & Visualization - PART 1</h>
<h3 align="center">:video_game: Fornite Ranking</h>

## Table of Contents:

- [Goal](#goal)
- [Motivation](#motivation)
- [Building](#building)
- [Part2](#insights)

---

## Goal

- Use an API (or API wrapper) to collect the data from one source;<br>
- Use raw web-scraping to collect the data from another source;<br>
- Store the results on your own database.

### Motivation

- On teh quarentine, I started to play Fortnite with my boyfriend and my friends.<br>
This motivated me to search about the best players of the game, and how many money them earns money just playing.<br>
Also, I wanted to compare my account score with my friends and with the pro-players.<br>
The motivated is fun, but we can take a deep analysis of the game with the data presented here.<br>

## Building

1°) Web Scraping to get the top 100 players - Fortnite<br>
Criteria of TOP: players who earned more money playing<br>
Source=<a href="https://www.esportsearnings.com/games/534-fortnite/top-players">Top 100 Fornite Players</a> <br>
<br>
2°) Web Scraping to get the top 101-200 players - Fortnite<br>
Source=<a href="https://www.esportsearnings.com/games/534-fortnite/top-players-x100">Top 101-200 Fornite Players</a><br> 
<br>
3°) Concatenate both columns;<br>
<br>
4°) Creathe a new column to format the columns "Player ID" <br>
<br>
5°) API to get the information about top players<br>
Data Cleaning (to remove columns with more than 80% null)<br>
Data Cleaning (to rename columns)<br>
<a href="https://dash.fortnite-api.com/">API Source <br></a>
<br>
6°)Merge informations (obtained by API and Web Scrap); <br>
Generate: top_players.csv<br>
<br>
7°)API to get informations about me and my friends;<br>
Data Cleaning (to remove columns with more than 80% null)<br>
Data Cleaning (to rename columns)<br>
Generate: top_friends.csv<br>
<br>
8°)Concat friends information with pro players informations (just to kid)<br>
Generate: top_and_friends.csv</br>
<br>
9°)Web Scraping to get Top 100 Highest Overall Earnings (players which earns more money from all games);<br>
Generate: highest_earnings_all_games.csv<br>
Source=<a href="https://www.esportsearnings.com/players/highest-overall">Top 100 Highest Overall Earnings</a> <br>
<br>
10°) Top 100 Highest Overall Earnings - Brazil<br>
Generate: highest_earnings_all_games_brazil.csv<br>
Source=<a href="https://www.esportsearnings.com/countries/br">Top 100 Highest Overall Earnings - Brazil</a><br>
<br>

7°) List of all DataBase exported to Excel:</br>
MAIN: top_players.csv<br>
MAIN: top_friends.csv<br>
top_and_friends.csv<br>
highest_earnings_all_games.csv<br>
highest_earnings_all_games_brazil.csv<br>
(Check Exported_Files path)

 
### Part2
Insights be analyse, by graphs, at Part II:<br>
 - Compare if the player which wins more money is the player with more kills per minute; <br>
 - Compare if the player which wins more money is the player with more kills per match;<br>
 - Analysing how many players with earns more money, earn it playing fortnite;<br>
 - Compare wich of my friends kills more, and compare us with pro players;<br>
 - Analyse how many brazilians it's on the top 100 of the world;<br>