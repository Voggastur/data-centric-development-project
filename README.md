# Hero Set

[Deployed website](https://voggastur.github.io/data-centric-development-project/)
[Project Repository](https://github.com/Voggastur/data-centric-dev-project)

The aim of this website is to present my skills in Python Flask and Jinja to present information from a backend database (mongoDB).


## Table of Contents

1. [UX](#UX)

    I. [User stories](#UX2)
    
    II. [Wireframes](#UX3)

    II. [Development Progress](#UX4)
    
2. [Features](#Features)
3. [Features for the future](#Features2)
4. [Technologies used](#Technologies)
5. [Testing](#Testing)

    I. [Testing functionality](#Testing2)
    
    II. [Testing user stories](#Testing3)

    III. [Bugs found](#Testing4)
    
6. [Deployment](#Deployment)

    I. [How to clone this project locally](#Deployment2)

7. [Credits](#Credits)


## 1. UX <a name="UX"></a>

The primary target audience are collaborators/employers who wish to see my knowledge in Python/Flask/Jinja.


#### I. User Stories: <a name="UX2"></a>

1. As an employer who recieved a link to Johans website, I want to see the page to see if it can handle backend database management, so that I can assess if he's eligible for a position NoSQL databases.

2. As an assessor I will judge the website on the totality of looks, documentation, testing, and functions among other things. I will take a particular look at the python file so that I can assess his score.

3. As a collaborator I want to see if Johan can be of use in a project, so I want to see Johans website. I will input some personal favourite hero and see if it shows up. Additionally I want to see the repository to evaluate the level of the code.

4. As a fan of roleplaying in Johans roleplay group, I want to update my heroes possessions of gold coins every round we play, because the game-master objected to my gold amount in an earlier game, and I want to show the truth


#### II. Wireframes: <a name="UX3"></a>

* [Wireframes.pdf](assets/wireframes/wireframe.pdf)


1. I struggled to come up with an idea for a website, but settled for this kind of character database website that had actually been on my mind for a while.
    I play roleplay games with a few friends from time to time, and one day I got the idea to make a website like this one.
    Although I don't see a commercial use as of now, it could be possible if I add a new user database collection with a login layout, so each hero could be connected to a user,
    who would have the sole privilege of editing his own creations.

1. I think the navbar with the replacing icons for mobile was implemented fine, as not to override the logo which switches to middle position on small screens.

2. The slider is a materialize component, and presents my website with images and captions explaining the purpose of the website

3. The cards are sorted as 2 in every row for large screens and 1 every row for small screens, a change from the 3 as shown in the wireframes.
    I felt that the content was too crowded for 3 so I changed it.

4. Materialize framework was used to achieve responsiveness

5. The website uses Jinja to import content into the base.html below the slider component and above the footer



#### III. Development Process: <a name="UX4"></a>

* I started by using some material from earlier pymongo projects we already developed, particularly the task manager project.

* I added a fourth link for the add_adventure template just as for creating heroes

* Every object in my project uses at least 2 functions, a template literal push and a movement increment. Movement increment was easy, however the pushing was difficult because of unfamiliarity with template literals.

* The moveAliens function took some time to learn how to move the whole array with a for loop, and not just single aliens. An if switch statement was later added to change directions as they touch the game boundaries.

* I learned alot during the development of this project, I had to read up on W3C articles everyday and I saw many youtube tutorials on similar projects, it has been a learning experience.

* Near the end of the project I removed unused constants like the gamescreen width and heights, and instead used fixed numbers where needed for spaceship move limits and alien move limits,

* I had a plan to implement spliced explosions in place for the aliens, with a short css animation to remove the explosion after 1s as well, but after some stonewalling and lost development time I dropped it out of scope for this project.


## 2. Features <a name="Features"></a>

* The website is an online storage of heroes for role-play gamers who meet from time to time to play through an adventure that one friend will be the storyteller of.
Upon completion of an adventure updating is needed for the heroes equipment and experience, and this is what the website is providing.

* 2 Collections were created in MongoDB in anticipation of the development project, originally I had less content per collection but I added some different aspects of each hero.

* Heroes can be read, edited and deleted from the front page, another tab in the Nav leads to the add hero page which presents a form to insert a new hero into the database

* Similarly Adventures can be read, edited and deleted from its' own link in the Nav, and similarly to add a new adventure you have to go to the Add adventure link

* As all aliens are destroyed, an alert is made to notify the player of the Win Game, and a location.reload() repopulates the game with aliens



## 3. Features for the future <a name="Features2"></a>

* An author MDB collection could be added which links heroes to the author that created them

* In addition I want to add a user login, so that editing of heroes could be restricted to the heroes that already have logged in session

* Less linear alien movement

* Exploding aliens, I should be able to splice them in the collisionDetection function, however I do not fully grasp everything I need to know yet

* collisionDetection for alien energybombs vs the player

* During my research I came upon other examples of similar games, and specifically another control scheme where something like .keydown(true) and .keydown(false) for each keyCode is used to determine when to move and not move the spaceship,
* I believe this is why these games have a superior sense of control of the playerobject, however it was deemed to complicated for me to include before submit date.

* Better winGame content, perhaps a new weapon for the next level, and a nicely styled HTML overlay rewarding the player who reached the winGame condition



## 4. Technologies used <a name="Technologies"></a>

* HTML5

* CSS3

* Javascript

* Github Deployment

* Gitpod IDE

* Google Fonts

* W3C Validator

* Autoprefixer

* Free Formatter


## 5. Testing <a name="Testing"></a>

#### I. Testing Functionality <a name="Testing2"></a>

1. I have done manual testing throughout the development process, because I didn't know how to implement test-driven-development effectively with jasmine in real-time.
2. As the game was finished I have continued to do some manual testing by playing around with it, I added limits to the spaceship movement late so that you don't move outside the gamescreen
2. However I have added a Jasmine test suite near the end of my development process to do (18) checks against my functions, objects, numbers and variables, this did actually provide me some insight into what I thought were arrays but were actually objects.
3. I have run the HTML code through [W3C HTML Validator](https://validator.w3.org) to check for errors in the code, none observed.
4. I have run the CSS code through the [W3C CSS Validator](https://jigsaw.w3.org/css-validator/) to check for errors in the code, none observed.
5. I formatted the HTML code through the use of [Free Formatter](www.freeformatter.com/html-formatter.html)
6. I added vendor prefixes to my css through the help of [Autoprefixer](https://autoprefixer.github.io/)


#### II. User stories testing <a name="Testing3"></a>

1. As an employer I go to see Johans game determined to see his skills, if he's really as good as he postulated in his CV.

    * I click the button to start the game, and try to shoot all the aliens.

2. As a collaborator I check out Johans game to evaluate his skills, to measure his eligibility for inclusion in my development team.

    * Click button to start the game, I will also go to google developer mode to check the console, and the source of the material.

3. As an assessor I go to Johans website determined to check every nook and cranny among which..

    * Play the game and shoot all the aliens.
    * Go through the javascript document to see if Johan follows coding conventions and proper semantics.
    * Make note of everything within the game.
    * Read through the extensive documentation.


#### III. Bugs found <a name="Testing4"></a>

1. As my rocket splices 2 aliens at the same time, a console error sometimes occurs "Cant read property of undefined aliens.top, on line 219 in game.js" which is in the Laser portion of the collisionDetection function, 
I think its a case of race condition where the laser for loop is trying to read the aliens.top property while it is being removed by the concurrent rocket for loop at the same time.
The error seems minor though, as the game continues without fault and both lasers and rockets can continue to splice the aliens for the remainder of the game

2. Alien energybombs don't have collisionDetection yet so will just fly through the player spaceship

3. I had an earlier bug with collisionDetection when the parameter + 30 had to be changed to - 70 and the next line -40 to yield an approximate hitbox,
I never sourced the cause of the bug but later tidying up of the other functions made my collisionDetection normal again, and so I just had to revert to + 30 again.

## 6. Deployment <a name="Deployment"></a>

This project was developed in Gitpod.
The project has been deployed to Github Pages - [Deployed Website](https://voggastur.github.io/interactive-frontend-project/)
The repository for this website can be found at this GitHub link: [Interactive Frontend Repository](https://github.com/Voggastur/interactive-frontend-project)

The following process was used to deploy the project:
1. Log into GitHub.
2. Select Voggastur/interactive-frontend-project
3. Select settings
4. Scroll down to Github Pages
5. Select Source: master branch
6. Retrieve the link to the deployed website

### How to clone this project locally <a name="Deployment2"></a>
​
To clone this project from GitHub:
1. At the top of this repository, click the green button **Clone or download**.
2. In the Clone with HTTPs section, copy the clone URL for the repository. 
3. Open your favourite terminal (cmd, powershell, bash, git bash, etc.)
4. Change the current working directory to the location where you want the cloned directory to be made.
5. Type `git clone`, and then paste the URL you copied in Step 2.
```console
git clone https://github.com/Voggastur/interactive-frontend-project
```
6. Press Enter. Your local clone will be created.



## 7. Credits <a name="Credits"></a>


* Spaceship and Alien pictures were taken from free library at flaticon.com.

* The energy, laser and rocket pictures were found in various picture archives via Google Search

* Scrolling background image was taken from NASAs website, but converted to a minimum size better suited to my website project

* The letters J and K for my favicon.ico were found on google picture search, upon finding them I combined them and made converted it into my favicon.ico.
