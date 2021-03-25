# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Ria Anand**

Time spent: **4** hours spent in total

Link to project: https://glitch.com/edit/#!/chestnut-tremendous-cardamom

## Required Functionality

The following **required** functionality is complete:

* [YES] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [YES] "Start" button toggles between "Start" and "Stop" when clicked. 
* [YES] Game buttons each light up and play a sound when clicked. 
* [YES] Computer plays back sequence of clues including sound and visual cue for each button
* [YES] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [YES] User wins the game after guessing a complete pattern
* [YES] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [NO] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [NO] Buttons use a pitch (frequency) other than the ones in the tutorial
* [NO] More than 4 functional game buttons
* [NO] Playback speeds up on each turn
* [YES] Computer picks a different pattern each time the game is played
* [NO] Player only loses after 3 mistakes (instead of on the first mistake)
* [NO] Game button appearance change goes beyond color (e.g. add an image)
* [NO] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [YES] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [YES] The time to guess on each turn increases as the pattern clue length increases

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](https://i.imgur.com/Gy0ghlj.gif)


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

I used the following links to troubleshoot and figure out how to implement the timer for each turn. I referenced other w3schools pages 
to learn the definitions and workings of certain javascript functions, html elements, and css features used in the program as well.
https://stackoverflow.com/questions/11837562/javascript-settimeout-wont-wait-to-execute
https://www.w3schools.com/howto/howto_js_countdown.asp
https://www.w3schools.com/js/js_output.asp

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

One challenge I encountered in creating this program was figuring out how to correctly implement the ticking timer. First, I used setInterval and could not figure
out why the function I passed in as a parameter was being called immediately, rather than after the specified delay time. After some research, however, I realized that
I was calling the function in setInterval since I put a "()" after the function name, rather than simply passing the function to setInterval so it could be called after 
the specified time delay. Another issue I had was figuring out where in the program to start and clear the timer. In order to properly do this, I had to understand the flow
of the entire program really well. After I figured this out, I started having an issue in which the timer stopped at 1 second rather than at 0, and after thinking about it I 
I realized this was because I had programmed the game to stop when the variable I had defined as "seconds" reached 0, but the value of "seconds" was displayed on the screen
with a 1 second delay, so when the value of "seconds" was 0, the screen still displayed 1. I solved this problem by adjusting my conditional statement in my code to stop the game
when the value of "seconds" was -1 instead of 0. Finally, I had some trouble figuring out how to start the timer AFTER the sequence was played, instead of during. At first, I 
I was really stuck but ultimately I solved this problem by passing the method I had defined as "startTimer" to setTimeout(). I used the "clueHoldTime", "cluePauseTime", and
"nextClueWaitTime" to calculate how much time a particular sequence would take, and passed that to parameter specifying the delay in setTimeout(). This way, "startTimer" would
only be called after the sequence had finished playing.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

After completing my submission, I've definitely become more curious about web development. I want to better learn the most common javascript methods and html elements that are useful for building the
functionality of a website. Getting more experience with the inner workings of a web game made me wonder how other complex webgames are implemented. For example, how does a game like tetris work? How does
the program create the different block shapes? How does the program detect when the block has reached the bottom? In addition, I was also curious about the big picture of the program. How did glitch.com run
the website? 

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

If I had a few more hours to work on this, I would add more features to the game. I like the idea of the playback speeding up after every turn, so I would definitely try to implement that feature.
In addition, I was thinking that it would be cool if the game had various levels. For example, maybe in level 1, the pattern would be 4 units long. If the user repeated this correctly, he would
go onto level 2, for which a new 8 unit long pattern would be generated. With each level, the pattern length could get longer and longer, until either cleared all of the levels or lost the game.


## License

    Copyright [Ria Anand]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
