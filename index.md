## Klopp and his Substitutions 
 
When Liverpool played Chelsea at Anfield which ended 1-1, Jurgen Klopp made some comments in the post match interview that caused a little bit of stir in the English press. The gist being that referee Micheal Oliver didn’t allowed Klopp to make a substitution and soon after that Willian scored in the 85th minute.<br>
<p align="center">
  <img src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/kloppoliver.jpg?raw=true" alt="profilepic"/>
  </p> 
<br>
But in general Klopp Substitution Strategy is quite different from other top 6 managers. Klopp believes in his attacking style of play and tries to alter the starting eleven when it reaches a point where his starting eleven needs something different or just some fresh legs. 
Klopp uses all 3 substitutes available quite often as his attacking style of is quite demanding and he needs his players to be ready for the next game.<br>
<p align="center">
  <img src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/index.png?raw=true" alt="profilepic"/>
  </p> 
<br>
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
X = pd.read_csv("...")
SUB = X["MATCH"].value_counts()
count_one = 0 
count_two = 0 
count_three = 0 
for x in SUB: 
    if (x == 1):
        count_one = count_one + 1
    elif (x == 2):
        count_two = count_two + 1
    else:
        count_three = count_three + 1
labels = 'One', 'Two', 'Three'
sizes = [count_one, count_two, count_three]
colors = ['gold', 'yellowgreen', 'lightblue']
explode = (0.1, 0.1, 0.1)
plt.pie(sizes, explode=explode, labels=labels, colors=colors, autopct='%1.1f%%', shadow=True, startangle=150)
plt.axis('equal')
plt.title("Subs made in for defending 1 nil lead in 2017/18")
plt.show()
```
One of things which have gone unnoticed by many is that Kloppo has changed his Substitution strategy in situations where team has to defend the three points rather than playing the attacking style football till the last minute. Jose Mourinho is widely criticized for his defensive style of play but one thing he is very good in making those defensive substitutions which basically are meant to kill the game and get all 3 points in the bag. Last season (2016/17)  Klopp was more stubborn in making a defensive change while defending a single goal lead as he relied on too much on his attacking ideology.

<p align="center">
  <img src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/2016-17.png?raw=true" alt="profilepic"/>
  </p> 
<br>
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
LAST = pd.read_csv("...")
kill_last_game = LAST.loc[(LAST["LIVSCOBF"] - LAST["OPPSCOBF"] == 1) & (LAST["MINUTE"] >= 75), ["SUBINPOS", "SUBOUTPOS"]]
Count_last_one = len((kill_last_game.loc[(kill_game_last["SUBINPOS"] == "Defender")]).index) 
Count_last_two = len((kill_last_game.loc[(kill_game_last["SUBINPOS"] == "Midfielder")]).index)
Count_last_three = len((kill_last_game.loc[(kill_game_last["SUBINPOS"] == "Attacker")]).index) 

labels = 'Defender', 'Midfielder', 'Attacker'
sizes = [Count_last_one, Count_last_two, Count_last_three]
colors = ['brown', 'green', 'orange']
explode = (0.1, 0.1, 0.1)
plt.pie(sizes, explode=explode, labels=labels, colors=colors, autopct='%1.1f%%', shadow=True, startangle=150)
plt.axis('equal')
plt.title("Subs made in for defending 1 nil lead in 2016/17", fontsize = 12)
plt.show()
```
But this season (2017/18) he has improved in this area by throwing in more defenders while defending a single goal lead. 
<p align="center">
  <img src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/2017-18.png?raw=true" alt="profilepic"/>
  </p> 
<br>
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
X = pd.read_csv("...")
kill_game = X.loc[(X["LIVSCOBF"] - X["OPPSCOBF"] == 1) & (X["MINUTE"] >= 75), ["SUBINPOS"]]
Count_one = len((kill_game.loc[(kill_game["SUBINPOS"] == "Defender")]).index) 
Count_two = len((kill_game.loc[(kill_game["SUBINPOS"] == "Midfielder")]).index)
Count_three = len((kill_game.loc[(kill_game["SUBINPOS"] == "Attacker")]).index) 

labels = 'Defender', 'Midfielder', 'Attacker'
sizes = [Count_one, Count_two, Count_three]
colors = ['brown', 'green', 'orange']
explode = (0.1, 0.1, 0.1)
plt.pie(sizes, explode=explode, labels=labels, colors=colors, autopct='%1.1f%%', shadow=True, startangle=150)
plt.axis('equal')
plt.title("Subs made in for defending 1 nil lead in 2017/18", fontsize = 12)
plt.show() 
```
This season Klopp has made the most substitution in this 2.5 year reign. One of the reasons is that is obviously Liverpool is involved in more than 2 competitions this season and other that Klopp has a more variety in selecting his starting 11. But one of the reasons why Klopp is a fan favorite and has a very good relationship with his players as well as ex players is that the trust level. 

<p align="center">
  <img src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/allsubs.png?raw=true" alt="profilepic"/>
  </p> 
<br>
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
X = pd.read_csv("...")
minute_count = X["MINUTE"].value_counts()
plt.figure(figsize=(10,5))
sns.barplot(minute_count.index, minute_count.values, alpha=0.8)
plt.title("Substitution in 2017-18 Season", fontsize=12)
plt.ylabel("Frequency of Substitution", fontsize=12)
plt.xlabel("Minute", fontsize=12)
plt.show()
```
Most of his substitutions are being made after 75th minute as he believes in his starting eleven and gives good amount of time for his players to make impact. 

### Lucky Substitutions 
Lucky Substitutions basically means those substitutions whose presence either makes a positive impact on the score line or brings a good luck factor. Though it may sound as a silly term in terms of football but luck factor does make a difference on the football pitch.  
<p align="center">
  <img src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/luckysubs.png?raw=true" alt="profilepic"/>
  </p> 
<br>
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
X = pd.read_csv("...")
Z = X.loc[(X["OPPSCOBF"] >= X["LIVSCOBF"]) & (X["OPPSCOAF"] < X["LIVSCOAF"]), ["SUBIN"]]
lucky_subs = Z["SUBIN"].value_counts()
plt.figure(figsize=(10,5))
sns.barplot(lucky_subs.values, lucky_subs.index, palette="RdBu_r", alpha=0.8)
plt.show()
```

### Unlucky Substitution
Unlucky Substitutions basically means those substitutions whose presence either makes a negative impact on the score line or brings a bad luck factor. Though it may sound as a silly term in terms of football but luck factor does make a difference on the football pitch.  
<p align="center">
  <img src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/unluckysubs.png?raw=true" alt="profilepic"/>
  </p>
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
X = pd.read_csv("...")
Z = X.loc[(X["OPPSCOBF"] >= X["LIVSCOBF"]) & (X["OPPSCOAF"] > X["LIVSCOAF"]), ["SUBIN"]]
unlucky_subs = Z["SUBIN"].value_counts()
plt.figure(figsize=(10,5))
sns.barplot(unlucky_subs.values, unlucky_subs.index, palette="BuGn_d", alpha=0.8)
plt.show()
```
