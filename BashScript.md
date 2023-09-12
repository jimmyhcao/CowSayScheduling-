<h1>Building The Script</h1>
<h2>Synopsis</h2>
Lucky Duck Casino provided me with several employee schedule files ranging from March 10 - March 17 where it listed employee names, hour worked, and casino game played (Blackjack, Roulette, Texas Hold'em). The schedule format was divided as shown below.
<br><p align="center">
<br>
<br><img src="https://i.imgur.com/Q2QtqHE.png" height="70%" width="70%">

Lucky Duck Casino requested a script that would be able to search for a <i> specific time, specific date, and specific game </i> 

<h2>Resolution</h2>
After understanding what is was being requested from Lucky Duck Casino and a familiar understanding of basic command line tools as shown in <a href="https://github.com/jimmyhcao/CowSayScheduling-/blob/main/README.md"> README</a>, we can begin to create a script to parse through the data to find any dealer working given the data, time and game played.

<h3>grep</h3>
<b>grep</b> as mentioned previously, can be used to search for matching patterns in text files. In this scenario we can use grep to search for the <b>$time</b> and <b>$date</b> being requested.<br>
<br>

```
grep $time $date_Dealer_schedule
```
<h3>awk</h3>
From there, we can use the <b>awk</b> command to filter out through the data more precisely to only print the columns we need. <br>
<br>

```
awk '{print $1,$2,$3,$4}'
```
