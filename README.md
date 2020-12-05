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

![SignIn](/Images/Signin.png)

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

__3. A Battle with Keys__

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

