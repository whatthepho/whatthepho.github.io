---
post_time: "10th Feb 2020:"
title: "4 months later and my second update. Customer to serve, an actual restaurant layout."
excerpt: "2020-02-10 - progress update"
toc: true
layout: posts
feature_image_path: "/assets/2020-02-11/cooking.gif"
---

## Huge delay between. But I will try to focus on this game from now on. I have registered for a steam page now.

![place-holder.png](/assets/2020-02-11/cooking.gif)

![place-holder_2.png](/assets/2020-02-11/organize.gif)

-----------------------
### Mon Feb 10 00:59:32 2020 +0200

### [Hotfix]Something is wrong with the table 2x1.

Which make it doesn't work (no collider, can't pick up, and also cause and array out of bound index if place in the edge of the map for no fucking reason. 

Also, update the UI Time Keeper so that the clock only animate if game is started.

-----------------------
### Mon Feb 10 00:53:52 2020 +0200

### [3hr]Add floor (yard) tiles and recycle tiles, ground work for buying/selling items. 

Makeshift start game function and some map designing. Trying to make the map prettier, so that I can create a introduction video about the game next Tuesday in the game dev meet up. 
Game look quite good (lol) now, so tomorrow, I will mostly just generate the materials for the websites and generate a video.

-----------------------
### Sun Feb 9 00:43:57 2020 +0200

### [4hr]Had a really productive day. 

Make chopping board locking (automatically chop and lock player in one place) again, spend 1 hr trying to fix a stupid bug related to that. 
Re-adjust the timer for cooking/waiting/chopping but it still doesn't feel right, yet. 
Add kitchen tile, wall tile and floor tile to the map. It looks functional, but it's quite ugly now. 
Also re-adjust the tutorial button panel a bit but still really ugly and out of place.

Spend most of the afternoon play Slay the Spire, so I pass like from ascension 1 to 4, but then I have a huge headache (probably from the stress from playing that game), so I went to sleep at like 4 and wake up at 7h30. Wife also made an awesome matcha-cheese cake, which is awesome.

-----------------------
### Fri Feb 7 00:50:58 2020 +0200

### [2hr]Add a GameData staic class to store some settings variable. 

Still not optimal, as I want each of these value to be object sepecific so the player can upgrade later. But, well, it's not for now. 
Also, add a shitty done version of the tutorial panel, where I display the basic instruction of the game. It's bad.

-----------------------
### Thu Feb 6 00:55:25 2020 +0200

### [2hr]Finish with the text popup for dining table.

They animate nicely when the user angrily leave the restaurant, or happily finish the meal. 
Add a quick hack button (press both triggers) to speed up the time (x3). 
Add a game timer UI to keep track of the time. Needs more works and refactoring though.
Also, took the dog to another vets hospital today to check her eyes issue. She got infected something and they give some medicine, but it costs us 169 euro, damn.

-----------------------
### Wed Feb 5 00:38:05 2020 +0200

### [1.5hr]FInish with the text popup animation. 
It's popup and fade out nicely now. Took a bit longer than I though because of a stupid bug regarding the Game interface. It's really late in the evening now so I have to go to sleep.
The reason for the change in the GameInterface UI is that, the animation there is counting up, from 0 to ANIM DURATION, but in the code, I want every timer to count from value, to 0. For consistency sake, so I rework that, and silly me, forgot some place thus, make it not working. Also help that yesterday I did a small refactor to that part, so it didn't work properly since yesterday ....

-----------------------
### Mon Feb 3 23:56:28 2020 +0200

### [1hr]Finish with the clock icon and danger icon for now. 
Also, add a very basic pausing functionality, which means, time stop (well, run at a 0.0001 rate) when ui is on.
The clock icon will animate faster when the countdown is closing to end. These code is a bit dirty and un-clean, but these code will be changed later anyway, so no need for clean code, just yet. 
Also, there was a weird bug yesterday where somehow after the first time its appear, the clock animation will appear BEHIND the progress bar, even though there is nothing wrong. Somehow, this bug doesn't happen today, which make no sense.

-----------------------
### Mon Feb 3 00:52:02 2020 +0200

### [2hr]Moving some asset files around a bit so it's a bit more organized. 
Create a clocking icon/animation to show all the timer task and a warning icon to so emergency timer. It's work in progress. Kind of works, but there is some bug and refactor needed.
Today, I played Overcooked 2 with my wife, it was pretty fun and challenging, which is perfect game, as I have tried some other coop game, such as Tools up, a overcooked like game but for moving house, which is okei, too easy, so we got bored after a while, and the main reason is that there is not much variant between rounds I guess. And Unrailed, which we also dislike, but because the game is too stressful, taxxing. Not super hard, but really stressful, which isn't nice.
Also, the dog got like health issue, like last week (last Sunday) I was playing with her and throw the floor ball into her face (we were playing catching), it looks fine at first, but then I think because she kept scratching her eye, it got some serious infection, so it got quite bad. We have put the collar of shame to her and wipe her eyes every few hours, but it got tired really fast because the dog kept waking us up mid night because her eye was really itchy, so we have to wipe her face for her. 4/10, not recommended, but an experience, nonetheless.

-----------------------
### Sun Feb 2 00:22:47 2020 +0200

### [1.5hr]Add a countdown mechanic for the dining table and the progress bar. 
It looks alright now, but I think I need to add sound to the game later, because it's kind of not feeling kind of bad now.
Good sound is needed I guess. But good new is the progress bar and the count down for the dining table works. I was planning to to it for the cooking pot as well, but it's a bit more difficult so it will be later.
Add a 2x2 pixel white box for all the progress-bar and pure color sprite, because the default sprite of unity somehow has a black edge, which annoy me a lot.
Now, I need to have a proper restaurant room, some art for the floor tile (should be easyer I guess, and maybe some art rework, and definitely good adjustment of the value for all the food/stuff.
For me, I have been playing non-stop slay the spire, which means I have completely finish the game with all 4 character, killing the final boss (the spire). So I guess my time for the game is done, but I think it's good time spent because I learn a lot of interesting rouge design tricks from that game.

-----------------------
### Sun Jan 26 23:45:52 2020 +0200

### [30min]Not much, opened the unity editor since 10.15, but only able to work for half an hour (it's 11.42) now, because I kept procrasting soo much.
It's Tet (lunar new year) holiday, so I was quite relaxed, and not in the mood of doing much. I also play a lot of video games (the true reason, lol), finish Yakuza Kiwami 1, finish watching the yakuza 0 story on youtube (it's an amazing story), and is starting Yakuza kiwami 2. 
Also, just downloaded Metro Exodus since it's on Xbox Game Pass pc and it's so cheap, like 1e/3 months, so I want to test the most demanding video game on my brand new pc. And somehow finally finish the true last boss of slay the spire, so yeah, mostly video game.
I also got super drunk on new year eve and vomit like a lot, really terrible, but I have been dirnking since soon (like 1 330ml bottle beer on lunch, 0.5 beer at the bar, and then in the eveing, 4 guys of us drink one vodka and one wiskey, but only I was vomitting, yeah..)

-----------------------
### Fri Jan 24 00:12:37 2020 +0200

### [2hr]Add a basic score system, ui to display said score and the player will have score added when the customer finish a meals (random from 20-40), just to test it. 
Next, will make a punishment system where if the customer waits to long, he will leave and player will lose score.
Add a scrolling number effect to the score count, so that it goes up slowly, not instantly, so that it looks cools. Unity Mathf.Lerp is weird, took a while to figure out.

-----------------------
### Sat Jan 18 21:52:01 2020 +0200

### [4hr]The button prompts thing works now, the game looks much more responsive already. 
Also some more refactor around the tween animator so we can use it for almost anything now. 
Small remap button so that [Y] now will pick up heavy item, instead of pressing both shoulder buttons.

-----------------------
### Tue Jan 14 21:58:00 2020 +0200

### [1hr]Add xbox buttons for more beautiful prompts.
I decided to chicken out of the gamedev meet-up. It's not like I have to be there and show up with anything, it's just a nice and relax evening to go there and talk with people, but I kind of too busy (it took like 40 mins from my home) and would took the whole evening, and well, since I have mom and wife, I don't really feel like hanging out and party-ing anyway.

-----------------------
### Sun Jan 12 23:28:21 2020 +0200

### [3hr]The progress bar bug is fixed. 

Also add a new state to the dining table component now, so it looks kind of ok-ish. It's sunday today and Tuesday there is a small game-dev meet-up and I kind of want to have the game to a play-able state to see how it works.
I will have roughly like 3 hours tomorrow to make the game play-able, which I don't think is enough. Let's see.
Great news is that I have a new computer now, which is awesome. It's super quick, and unity compile code a lot faster now, which mean writing code and then live test in Unity feels a lot better now. Also, gaming on this beast feels good. PUBG max everything and stable 60fps, what a dream.

-----------------------
### Thu Jan 9 00:13:42 2020 +0200

### [1hr]Trying to fix a bug cause by rendering offset, in which, object placed onto table will be moved a bit for the offset, but the progress bar isn't moved. 
Which, I tried to solved by making the progress-bar inherit from the rendering-component as well. This might be good as it also solve the zDepth thing as well. Temporary just wrote it down here, I might finish it tomorrow as it's late today and I won't do anything anymore.
My pc parts came, everything, except the case, so I have to wait. Terrible feeling. My new PC is decent. Ryzen 3600x, RTX-2070-SUPER ASUS ADVANCED, 1tb SSD and 2TB HDD (awesome, I won't lack storage space anymore). 16gb RAM and a way overkill PSU whic is 850W, almost twice as much the required power, which will be super silent. Which is nice I guess. The case is pretty nice too, has some RGB and glass window so you can see the RGB inside as well.

-----------------------
### Tue Jan 7 00:11:35 2020 +0200

### [2hr]The looping animation works now. 
It's nothing wrong with TWEEN or anything, just that it's a mis-colon, the animation time was 0.15 second, but then I typed it to 015 seconds (without the dot), that's why the animation nevers loop for me, because it took 15 seconds so I never see it works again.
Then, after like serveral rewrote, I see the typo and then even just the original animation works anyway, but it's kind of too late because I already wrote a new file and all. Stills, I guess this is better because it makes the code cleaner.
This Friday, there is a gamedev meet-up event in Helsinki, and I plan to go there, so I will need to make the game a bit ready and presentable, like a tutorial, maybe some menu and score tracking to make it fun, a menu to spawn object.
And tomorrow, my new pc parts will arrive, like all of them, except the computer case. Really bullshit, somehow ordering all the way from Germany and it arrived in like 3 days, where ordering just within Finland and it took a whole fucking week.

-----------------------
### Mon Jan 6 00:25:42 2020 +0200

### [2hr]Kind of refactor the FoodContainer, looks ok-ish now, but the looping Tweening animation for that doesn't work yet.
This is due to the fact that, when I place a CookingPot on top of Stove, 2 animations script (TWEEN) are created at the same time: The shrink in/out whenever we pick/drop object. And the Shrink up when we cooking, thus make it doesn't animating. Which make me really frustrated about this. Dunno what I will do though, this is annoying, trying to solve it smartly using callback but doesn't work, maybe I have to use a time check inside update function to do this. But this will be a bit ugly.

-----------------------
### Sun Jan 5 02:11:52 2020 +0200

### [2hr]Some refactor on animation script to make things cleaner and add a new animation for food being cooked and overcooked.
Now, try to refactor the FoodContainerComponent by adding the progress bar to each and every food container component, and maybe some logic related to cooking/dining serving there as well, maybe it feels more natural? I don't know. Will do more tomorrow, as today I have a poker night so I didn't have much time to code (I'm also procrastinate a lot as well).

-----------------------
### Fri Jan 3 00:32:04 2020 +0200

### [1hr]Kitchen-sink now fully works. 
Things look a bit sluggish, so maybe I will bring back the locking player mechanism for chopping/cleaning. 
It's way more fun that way, but I will still keep the part of pressing X to make it faster to make the game more exciting, but the value will be really low, like if you passively cleaning a board take 5s, then mashing button while passively doing it should only increase it to 3s. 
Also, more ideas about animations and stuffs.
Got a full day off yesterday (1st day of the year) but I didn't do much because I was too busy trying to build my NEW COMPUTER, yay. It's nothing too fancy though, but it's a nice upgrade from my current laptop.

-----------------------
### Mon Dec 30 23:27:02 2019 +0200

### [1.5hr]Makes some tweening animation to separate the feedback between [A] pressed (pick/drop item) and [X] pressed (interact with items). 
Feels better to me now, but that really doesn't count because I'm the one making it. Still, at least, for me, the game feels better.
Next, will do a few more animation, one for the object that is being processed automatically (ie, stove cooking pot, dining table eating bowl), and one kind of alarm animation, like over-heating pot, so, it's shaking.
Also, needs to finish the kitchen-sink, fix the sorting layer of the player cursor, update to a better cursor, have a better floor texture, and add some UI so it actually feels like a game. And it will be like a good MVP that is capable of demo-ing to people. (oh, and tons of variable tweaking, so that it feels nice)

-----------------------
### Mon Dec 30 00:27:11 2019 +0200

### [2hr]Add the kitchen-sink to clean the dirty dish/bowl. 
Kind of works right now, but we need to add the progression system to the dishwashing.
Fix a super crittical bug related to the dropping object, which I made just the otherday, thinking I would optimize something, but actually, I just make more fucked up. It's related to Food container null check and all the condition of dropping to stove/dining table ....
Add some more animation so the game feels more responsive. I think the game, even at this very prototype stage, still needs a bit more animation, so that each button/interaction feel responsive.

-----------------------
### Thu Dec 26 15:18:49 2019 +0200

### [1hr]Add a new flag to lock pickable object so that they can't be picked if being locked. 
This is currently used to lock food container while it is being eaten on the dining table.

-----------------------
### Wed Dec 25 23:21:13 2019 +0200

### [1.5hr]The dirty bowl works. 
After the food is served at the dining table, it will be transformed into a dirty bowl, which needs to be cleaned. 
Right now, it can be clean by just drop everything to trash can. Will fix later. 
Right now, it seems there are some un-clear case and bug fix, so maybe I will focus on that.

-----------------------
### Tue Dec 24 00:34:00 2019 +0200

### [0.5hr]Small removal of un-used class and unnecessary code. 
I bough a new 27 inches samsung monitor, and spend the night watching the witcher movie. first 2 eps are good.

-----------------------
### Sun Dec 22 23:34:44 2019 +0200

### [0hr]Forgot to add these changes to the previous commit.

-----------------------
### Sun Dec 22 23:34:14 2019 +0200

### [1.5hr]Working on the dirty sprite for the Bowl. 
Finish with the art (look okei-ish in my really low standard). Have some code in place, needed for implementation next time I try to work on this code (hopefully tomorrow)

-----------------------
### Sat Dec 21 22:02:24 2019 +0200

### [1hr]Trying to get back to the groove. 
Still too much procrastination, but did some small thing, like a small foundation for the animation to have better feedback, and small quality of life update where you can have a bowl, and get the food object to the bowl directly, while holding the bowl, looking at the pot. 
Previously, the bowl has to be on table and you have to hold the pot and pour it to the bowl. Hopefully, tomorrow I can make more code.

-----------------------
### Tue Dec 10 22:26:54 2019 +0200

### [15 min]This commit is mostly just a spiritual commit, like, one that say, ok, I should get back to making this video game now. 
Lots of things happen during the 6 or 7 weeks I haven't pushed anything. I tried to get used to my new job, get ready for the huge trip back to my home country (vietnam), prepare for the huge weeding, have a honey moon in Japan, and go back to my current resident country.
But, I am all set now, so I will try to start working on this game, again.

-----------------------
### Wed Oct 23 00:29:14 2019 +0300

### [1.5hr]Finished most of the functionality of the dining table. 
The gameplay loop for dining table now is:
Idle ->Press X to generate a random order->Display the food prompt (Waiting for Dish)->Exact food is served->Eating process (Eating)->Finished (Completed)->Pick up dish from table->Back to Idle.
Fix some bugs and make that you can't place anything on the dining table except the correct food. Code is quite similar to the Stove Component.
It's done functionality now but the gameplay is quite bland, some polish/interaction feedback is needed and probably some bug fixxing as well.

-----------------------
### Tue Oct 22 00:32:12 2019 +0300

### [2hr]More work on the Dining table, just more tighter control and create room for future works.
I think it's getting there and it's quite fun to play now. Just need a small score system and some timer on things, and it can keeps going for quite fun.
Also, tons of quality of life and general animation and improvement needed to make the game more clear and more responsive.
Remove DoozyUI as it's huge size make compilation time slower, which is annoying.
I still got a lot of procrastination on me, but at least I'm doing more than I did yesterday, so it's improving.

-----------------------
### Sun Oct 20 01:02:05 2019 +0300

### [1Hr]Continue working with the Dining table. Now it can receive food, and check that if the requested food is valid.
Add a small prompt to show that the users should go and press [X] at the table to request an order. It's coming together as this is quite fun to play now.
I was starting Unity at like 5pm and now it's 1am, and I have only actually have 1hr to work with it. Too much distraction and procrastination. Hope that I will be able to finally come to my sense and be a bit more productive :(

-----------------------
### Wed Oct 16 00:20:11 2019 +0300

### [3hr]Halfway through the dining table. 
I actually did like 1 hr of work yesterday, but if was really incompleted, there is even a compile error so I don't feel like committing.
Finally got the discipline (?) or motivation to sit down and code for a long time without being distracted by anime/manga/something else. You can sort of walk to the table, press [X] and then the table will generate an order. Tomorrow will make it validate the order and check if the order is actually correct.
Some refactor on the interactable component so that it makes more sense. Many more refactor in some other part of the code, mostly food and recipe related stuffs, because somehow the code I wrote 2 months ago doesn't make sense now. Slowly coming together though, so it's nice.
I got a new job, game programmer at a government company, so I have been mostly spending time saying goodbye to the old companies, 2 farewell parties, and something else. Also took wedding picture with my future wife and I went and played with a local music club on Sunday, which was super nice.

-----------------------
### Thu Oct 10 00:55:25 2019 +0300

### [1.5hr]I was mostly procrastinating, but add some underline code for dining table and a pop-up UI, which we should press X at the empty dining table, and it should display on a popup UI the desired dish.
Decide to also not use the DoozyUI since it's not needed for now, maybe later when I actually have UI and menu and what not. It looks OK, just that not what I need right now.
Somehow the procrastination got the better of me and I spend most of my time reading manga. Since the last commit, I actually read shit tons of things. Here are the thing I read:

+ 140 chapters of Domestic girlfriend (it's good, but it's really heavy in a sense that I am sooo invested in Rui (the smaller sister), that when she got together with the MC, I'm so happy and was sooo annoyed, during the build up for that. I really have to stop because it's too tense and I was honestly emotionally invested, happy, sad and stuffs like that.
+ Boku girl: A gender bender manga where the main char that normally looks like a girl, is actually turned into girl by magic, and his/her path to find his/her true identity. Finished it in one day (like, discovered it at work at 4pm and binge through the entire thing (107 chaps) until like 1 am. Really good, make me think a lot about gender identity and all the thing.
+ I want to eat your pancreas: heart wrenching, tear wrecking, it's like, in top 5 anime movie and it's really good, I read the manga, which I think is the even better version, maybe? It's really touching story and leaves me with a lot of things to think about.
+ Bokura no hentai: It's not a hentai. It's a gender bender manga about 3 girls, 2 cross-dressing for reasons and a trans girl. It has a lot of recommendation but I dropped it after 10 chapter because it is too depressing.

-----------------------
### Thu Oct 3 20:22:34 2019 +0300

### [1Hr]Add Doozy UI package for awesome UI. Looks neat. 
I bought it from Humble bundle, but this seem like a good purchase. Update the dining table art so it looks slighly better.
Installation process for Doozy UI takes quite a while and I have to update the DOTween as well, feel really lazy today so I didn't do much. I will try to learn DoozeUI tomorrow I guess.

-----------------------
### Fri Sep 27 23:40:41 2019 +0300

### [1.5hr]Add the dining table, some some base code for it. 
Right now, just log if you put something that is not food, and if you put a servable food container, it will empty that.
Tomorrow, I will go for a vacation in Germany for OktoberFest. Flight at 5.35 in the morning so I don't know if I even got to sleep or not. Trying to download some anime to my iphone to watch on the fly but it's really tricky. Fuck apple.

-----------------------
### Fri Sep 27 00:10:00 2019 +0300

### [1hr]The sorting layer works as I wanted now. 
So, I also finished doki doki literature  club yesterday.
It's a really nice awesome game and really short, only 3hr, really recommend it (eventhough I should stop playing game and finish making this game). I will have a small vacation (lol) in the next 4-5 days, but I promise that afterwards, I will focus 100% on the game now. (Until I found another game that caught my attention). I'm looking at Catherine Classic, as well as persona q2, but they are much shorter than p5 and I doubt that they would have the same pull power as p5.

-----------------------
### Tue Sep 24 21:36:54 2019 +0300

### [1.5 hour]Making the player render properly behind all objects. 
However, it's till a bit glitchy and I'm not satisfied with it yeat.
I still haven't finished the damn persona 5 game yet, but I am quite close. 90 hours clocked in. I'm think I am at the final boss section now. I heard there are like 5 endings, 3 bad ones, 1 good one and 1 true ending. Hope that I'm going to reach at least the good one.

-----------------------
### Sun Sep 15 15:37:33 2019 +0300

### [2hr]Trying to make the sprite sorting layer works with the grid pos (x, y).
It works and I managed to find and fix a bug related to the grid issues so it's quite nice. Objects are now displayed correctly. But the player hasn't. Will update the player next, just that I don't feel like coding now, so I am off to play more Persona 5. Maybe I will code more in the evening.
I'm also have a cold from the start of the week so I'm still feeling quite bad about it.

-----------------------
### Wed Sep 11 22:52:50 2019 +0300

### [1h]Working on sorting lay to fix a display issue, where object further away are rendered on top of object closer.
For example: Player is standing behind the table, but is rendered on top of the table. Learn about sorting layer in sprite-renderer. Right now, just sorted based on y value, but I think using grid y value would be a better choice.
Stop for now, I was really hooked with Persona 5, clocked almost 60 hours so far and is at the 5th (bigbag burger) palace and is in a relationship with Ann Takamaki. Really nice game.

-----------------------
### Tue Sep 3 22:02:47 2019 +0300

### [1hr/1hr other day]Add a wall surrounding the map, and add a sprite for dining table of the customer.
Add surrounding so the player can't go outside and add proper code to check for out of map input, instead of just let Unity post an error like this.
Add a dining table, which is just normal table with a cloth on top of that.
I have been so lazy recently because I have been playing Persona 5 non-stop. Have like 26 hours on that game so far. By now, I think I have see and learn all the interesting and cool mechanic about the game, but the gameplay and story is soo good, just kept me wanting to go back for more.
