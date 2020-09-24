<p align="center"><a href="https://imgbb.com/"><img src="https://i.ibb.co/L0C0q84/IMAGE.jpg" alt="IMAGE" border="0"></a></a></p>
<h1 align="center">:small_blue_diamond: Data Gathering & Visualization - PART 1</h>
<h2 align="center">:video_game: Fornite Ranking</h>

## Table of Contents:

- [Goal](#goal)
- [Motivation](#motivation)
- What is Fortnite?(#What is Fortnite?)
- [Building](#building)
- [Part2](#part2)


---

## Goal
What is the Fortnite pro-players profile?

## Motivation
- On quarentine, I started to play Fortnite with my boyfriend and my friends.<br>
This motivated me to search about the best players of the game, and how many money they earns just playing.<br>
Also, I want to compare my account stats with pro-players.<br>

## What is Fortnite?
It's a FPS Game, where you need to shot and to construct to deffend yourself.<br>

## Step-to-Step

- Use raw web-scraping to collect who are TOP 25 players classified at Fortnite's World Cup;
- Use an API (or API wrapper) to collect the data about TOP 25 players classified at Fortnite's World Cup.<br><br>
- Store the results on my own database.

### Motivation

## Building

1°) Web Scraping to get the top 25 players - Fortnite<br>
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

 
### Part2
Options to be analyse, by graphs, at Part II:<br>
https://public.tableau.com/profile/leticia.fossato#!/vizhome/Proj-Fortnite/Histria1?publish=yes
