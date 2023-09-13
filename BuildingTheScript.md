<h1>Building The Script</h1>
<h2>Synopsis</h2>
Lucky Duck Casino requested a script that would be able to find the employee working given a <i> specific time, specific date, and specific game </i>. The files that Lucky Duck Casino provided me with were several employee schedule files ranging from March 10 - March 17 where it listed employee names, hour worked, and casino game played (Blackjack, Roulette, Texas Hold'em). The schedule format was listed as shown below.
<br><p align="center">
<br>
<br><img src="https://i.imgur.com/Q2QtqHE.png" height="70%" width="70%">


All files used during this project can be found in the <a href="https://github.com/jimmyhcao/CowSayScheduling-/tree/9ebe6637b3333db4bce773749f3db807e3a12590/Downloads"> Download</a> folder for reference.



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

However, it should be noted that the 3rd and 4th column printed is dependant on which game is being requested as we can see from the above sample schedule that 

<li>Blackjack appears on $3, $4
<li>Roulette appears on $5, $6
<li>Texas Hold'em appears on $7, $8 </li>

<br>Therefore, we would need the script to read user input and modify its search based on what was entered through the use of the <b>read</b> command. 
<br>
```
"Which game? (enter 1,2,3,)"
echo "1 - Blackjack"
echo "2 - Roulette"
echo "3 - Texas"
echo
read game
```

<br>Then depending on user input from the step above, the script can choose the correct column to print out.
<br>
```
case $game in
        1)echo "$date" Blackjack Dealer; grep "$time" "$date"_Dealer_schedule | awk '{print $1,$2,$3,$4}';;
        2)echo "$date" Roulette Dealer; grep "$time" "$date"_Dealer_schedule | awk '{print $1,$2,$5,$6}';;
        3)echo "$date" Texas Dealer; grep "$time" "$date"_Dealer_schedule | awk '{print $1,$2,$7,$8}';;
esac
```

<br> Finally, applying the same concepts of the <b>read</b> command stated earlier for the <i>time</i> and <i>date</i> requested and using the <b>cowsay</b> command into the script to make the user experience more whimsical, we end up with the final script of:
<br>
```
!#/bin/bash

cowsay "Find dealer by date, time, and game"
echo
cowsay "Enter the  date (MMDD)"
echo 
read date
echo 
echo
cowsay "Enter the time (HH:MM:SS AM/PM)"
echo 
read time
echo
echo
cowsay "Which game? (enter 1,2,3,)"
echo "1 - Blackjack"
echo "2 - Roulette"
echo "3 - Texas"
echo
read game
echo
case $game in
        1)echo "$date" Blackjack Dealer; grep "$time" "$date"_Dealer_schedule | awk '{print $1,$2,$3,$4}';;
        2)echo "$date" Roulette Dealer; grep "$time" "$date"_Dealer_schedule | awk '{print $1,$2,$5,$6}';;
        3)echo "$date" Texas Dealer; grep "$time" "$date"_Dealer_schedule | awk '{print $1,$2,$7,$8}';;
esac
```

We now have a simple script that will display the name of an employee working given the date, time and casino game played 

<br><p align="center"><i>Video demonstration of script in use</i>


https://github.com/jimmyhcao/CowSayScheduling-/assets/132900530/f6404783-0271-4c35-b5b7-1206a1e720b4







