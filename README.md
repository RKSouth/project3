# Project X

![ProjectX](./client/public/Images/gameOn.png)


## Table of Contents
* [Deployed Site](Deployed)
* [Technologies Used](Technologies_Used)
* [Description](Description)
* [Complications](Complications)
* [Features](Features)
* [Usage](Usage)
* [Author](Author)
* [Credits](Credits)
* [License](License)

## Deployment

[Deployment](https://desolate-crag-53628.herokuapp.com/)

## Technologies Used 

* Javascript
* React
* HTML/CSS/Bootstrap
* NPM
* SQL/Sequelize

## Description

This app was created to make a fun, exciting battle game so users can pass time. A user begins by signing up with an email, username, and password. They are redirected ot a screen including a leaderboard and user information. At the bottom there is a button to guide the user to begin the game. Once the game begins the user is prompted to choose their champion! The CPU is chosen at random and the battle begins. Once either the user or the CPU reaches health of 0, then the game is over.

This game was inspired by Rock Paper Scissors, but made with 5 choice options instead of 3. 

## Features

__1. A Sign-in/Log In__

*What*

![SignIn](/Images/SignIn.png)

A part of the page that allows users to sign-up or log in to gain access to a personalized page with their information, the games leader board and allows them to play the game.

*Why* 

So that your data can appear on the leader board and you can view your user data

*How?*

Technologies:
* passport.js
* bcrypt - to keep passwords private
* local storage - to transfer data easily from one page to another
* mysql/jawsdb - to keep long term storage of users for use in the leader board
* axios - to make calls to routes that then connect to the database


Keep note: Log in function currently unavailable only sign in works

__2. A leader board and User data__

*What*

A board that displays user stats and the leader board

![SignIn](/Images/stats_leaderboard.png)

*Why*

To put it simply -we play to win!

*How*

I used local storage to hold the username that was logged in and then compare it to what was in the database. If that user was in the database then we get user stats for them.

![SignIn](/Images/userbaord.png)

For the leader board we just pulled all the user data and then used a sort function to display it. I made sure to add functionality for both the wins and losses. 

![Sorting](/Images/sort.png)

__3. A Character Selection__

*What*

Before the battle opens, A user selects a character that they will play with.

*Why*

So users can have a dynamic game play experience by choosing different characters with different attacks in order to see which one would win

*How*

This is one we went back and forth with, it works just fine with the database-however because it isn't "dynamic" or changeable yet we opted to write a json file to call to instead. As you can see in order to link the attacks and the characters in the json file we needed a number for each attack- each character has 5 attacks, numbered 1 through 5, and each character has it's associated attack number (see below).

![Sorting](/Images/character.json.png)

Then we have to retrieve the characters from the json. This was accomplished by simply importing and setting a set state

However the routes are there and everything is built. Also take note of the constant set on line 10, determining where where we are in the state of play. Most importantly though you can see this code getting the characters and looking at their attacks using the function, selectCharacter(). within the class. Below in selectCharacter() we then select cpu attacks and set the state.

![Characters](/Images/characters.png)

Finally, we render the characters- you may, at this point wonder why I am going into such detail here. And to that I say, because it's so cool!! 

In the render characters section we use the game state to determine what should load and when, I know, awesome right??

![Coolstuff](/Images/whattolookat.png)



__3. A Battle with Keys__

*What*

A battle that gives you multiple choices of attacks, and returns a result - the result being the opponents' attack, the name of the opponent's attack and the result of the battle (whether it be a draw, loose 2, win 2, loose 1, win 1). The points are decremented based off of the outcome until either opponent reaches zero. 

*Why*

I don't have the greatest explanation as to why the game functions this way in particular because I did not write this section of code. I can only say really, because Ry wanted it that way. I did propose a decrementing structure to begin with - but he flushed it out. He spent a lot of time thinking about game dynamics and how to make it fun and engaging and this is what he came up with. 

*How*



__4. For Future Development__

* A log out button - not entirely necessary but nice to have

* A button that allows you to play another game without reloading the website

* An animated fight -because animation is better

* A different database because I am sick of mysql and would like to learn how to use graphsql

* The ability to add your own characters -it may conflict with animation but whatever. 

* The ability to select your background and have it influence the outcome of the fight -this was Wess's idea and I think it's brilliant and I want to do it!

* More dynamic character cards that maybe display the attacks related to the character

* A series of fights with power-up mini games in between. This was Ry's idea but we had to scrap it due to time.

## Complications

Some complications faced in this application was saving user data once logged in.

# Authors

Jennifer Henry

[Github](https://github.com/jenryhennifer) ||
[LinkedIn](https://www.linkedin.com/in/jennifer-henry-4a540a149/edit/add-link/) || 
[Portfolio](https://morning-ridge-20215.herokuapp.com/)

Ry Hull

[Github](https://github.com/ryandelonhull) || 
[LinkedIn](https://linkedin.com/in/ryan-hull-94003144) ||
[Portfolio](https://ryandelonhull.github.io/Repo-React-ion/)

Rachael Kelm-Southworth

[Github](https://github.com/RKSouth) ||
[LinkedIn](https://www.linkedin.com/in/rachael-kelm-southworth-87a3831b3) ||
[Portfolio](https://rksouth.github.io/React-Portfolio/)

Earnest Wesson

[Github](https://github.com/HEEM86) ||
[LinkedIn](https://www.linkedin.com/in/ernest-wesson-b4183b5a/) ||
[Portfolio](https://github.com/HEEM86/ReactPortfolio)

## Credits

I would like to thank Kerwin, Manuel, Roger, Jerome, Mahi and all my classmates. Manuel, a man of infinite patient, Kerwin, for always bringing me back down to Earth and reminding me of who I am, Jerome who reminded me to stay on task and helped me stay focus on my goals, Roger for getting mired in the details of the code with me, Mahi for being able to examine the situation and prove that it works! 

To my project group:
 Ry who built the battle function, your work ethic, drive and steady hand are are absolutely going to take you places. Wess, who designed the front end and implemented it, your creativity and drive are amazing, you never let up and your calm lo-fi demeanor was great to be around. Finally, Jenn who held my hand, hooked the front end up to the backend and built our user sign in, thank you for your support and willingness to take me on and guide me throughout our process.

## License
[MIT](https://choosealicense.com/licenses/mit/)

