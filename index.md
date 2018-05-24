<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<style>
button.button {
  border-radius: 4px;
  background-color: #777772;
  border: none;
  color: #FFFFFF;
  text-align: center;
  font-size: 13px;
  padding: 5px;
  width: 70px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}

button.button span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

button.button span:after {
  content: '\00bb';
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

button.button:hover span {
  padding-right: 15px;
}

button.button:hover span:after {
  opacity: 1;
  right: 0;
}
body {font-family: Arial, Helvetica, sans-serif;}

#myImg {
    border-radius: 5px;
    cursor: pointer;
    transition: 0.3s;
}

#myImg:hover {opacity: 0.7;}


.modal {
    display: none; 
    position: fixed; 
    z-index: 1; 
    padding-top: 100px; 
    left: 0;
    top: 0;
    width: 100%; 
    height: 100%; 
    overflow: auto; 
    background-color: rgb(0,0,0); 
    background-color: rgba(0,0,0,0.9); 
}


.modal-content {
    margin: auto;
    display: block;
    width: 80%;
    max-width: 700px;
}


#caption {
    margin: auto;
    display: block;
    width: 80%;
    max-width: 700px;
    text-align: center;
    color: #ccc;
    padding: 10px 0;
    height: 150px;
}


.modal-content, #caption {    
    -webkit-animation-name: zoom;
    -webkit-animation-duration: 0.6s;
    animation-name: zoom;
    animation-duration: 0.6s;
}

@-webkit-keyframes zoom {
    from {-webkit-transform:scale(0)} 
    to {-webkit-transform:scale(1)}
}

@keyframes zoom {
    from {transform:scale(0)} 
    to {transform:scale(1)}
}

.close {
    position: absolute;
    top: 15px;
    right: 35px;
    color: #f1f1f1;
    font-size: 40px;
    font-weight: bold;
    transition: 0.3s;
}

.close:hover,
.close:focus {
    color: #bbb;
    text-decoration: none;
    cursor: pointer;
}


@media only screen and (max-width: 700px){
    .modal-content {
        width: 100%;
    }
</style>
<button style="margin-right:10px; margin-left:170px" onclick="window.location.href='https://raffa1996.github.io/5yards5feet'" class="button"><span>Home </span></button> |  <button style="margin-left:10px; margin-right:10px" onclick="window.location.href='https://raffa1996.github.io/Apps'" class="button"><span>Apps </span></button> | 
<button style="margin-left:10px" onclick="window.location.href='https://raffa1996.github.io/Projects'" class="button"><span>Projects </span></button><br>
## Klopp and his Substitutions 
 
When Liverpool played Chelsea at Anfield which ended 1-1, Jurgen Klopp made some comments in the post match interview that caused a little bit of stir in the English press. The gist being that referee Micheal Oliver didn’t allowed Klopp to make a substitution and soon after that Willian scored in the 85th minute.<br>
<p align="center">
  <img id="myImg" src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/kloppoliver.jpg?raw=true" alt="profilepic"/>
  </p> 
  <div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="caption"></div>
</div>
<script>
// Get the modal
var modal = document.getElementById('myModal');

// Get the image and insert it inside the modal - use its "alt" text as a caption
var img = document.getElementById('myImg');
var modalImg = document.getElementById("img01");
var captionText = document.getElementById("caption");
img.onclick = function(){
    modal.style.display = "block";
    modalImg.src = this.src;
    captionText.innerHTML = this.alt;
}

// Get the <span> element that closes the modal
var span = document.getElementsByClassName("close")[0];

// When the user clicks on <span> (x), close the modal
span.onclick = function() { 
    modal.style.display = "none";
}
</script>
<br>
But in general Klopp Substitution Strategy is quite different from other top 6 managers. Klopp believes in his attacking style of play and tries to alter the starting eleven when it reaches a point where his starting eleven needs something different or just some fresh legs. 
Klopp uses all 3 substitutes available quite often as his attacking style of is quite demanding and he needs his players to be ready for the next game.  
<br>
<p align="center">
  <img id="myImg" src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/index.png?raw=true" alt="profilepic"/>
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
  <img id="myImg" src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/2016-17.png?raw=true" alt="profilepic"/>
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
  <img id="myImg" src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/2017-18.png?raw=true" alt="profilepic"/>
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
  <img id="myImg" src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/allsubs.png?raw=true" alt="profilepic"/>
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
  <img id="myImg" src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/luckysubs.png?raw=true" alt="profilepic"/>
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
  <img id="myImg" src = "https://github.com/raffa1996/Klopp-and-his-Substitutions/blob/master/Asset/unluckysubs.png?raw=true" alt="profilepic"/>
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
