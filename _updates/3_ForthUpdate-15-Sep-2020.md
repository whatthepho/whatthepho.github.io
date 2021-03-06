---
post_time: "14th Sep 2020:"
title: "Forth update. Updates after six months. Food processor, lots of refactors, some new art, and planning to change the game to 3d!"
excerpt: "2020-09-15 - Progress update"
toc: true
layout: posts
feature_image_path: "/assets/2020-09-14/restaurant.gif"
---

+ Now, there are proper end-game screens that separate the days into different stages (Preparation -> Restaurant open -> Closing (wait for the last customer to finish) -> Next day). Thus, the idea of a stage/level in a rouge-like scene. So, you climbing/progressing by going to the next day.

+ There are probably a lot of under-the-hood code and refactoring, that I really forget what I have done.

+ There are some new assets, like food processor, making all object has the progress-bar/popup component for ease of development, and just some coding improvement that I think that would make this project more managable

+ I'm thinking of changing this game into a 3d game because my art-skill is crap anyway, so I will just survive of buying assets from the unity store, so I can find more source in 3d, so the quality is better, and with some good shader magic, I can blend thing together and make things more format. Not to mention, 3d would be more beautiful (for my art-skill) and I can avoid a lot of just 2d rendering/layer/sorting problem that wouldn't happen in 3d. And maybe, I can try to add RTX support, as far as I know, Unity supports it so why the not, if I have the time and it's simple enough?

+ Totally unrelated, but in the span of half a year, I bought my first car (a 2006 Toyota Avensis, love every moment of it), watching my son going to be in this world (in like 5 weeks) and moved to a bigger and I guess, more permanent apartment.

+ Anyway, here's the progress.

![image.png](/assets/2020-09-14/restaurant.gif)

+ Food processor!

![image_2.png](/assets/2020-09-14/processor.gif)

+ End screen menu, it's not much, but it's something

![image_3.png](/assets/2020-09-14/end_screen.gif)

-----------------------
### Tue Sep 15 00:38:33 2020 +0300



### [4hr]Create another progress update, which contains one build, some gameplay gifs, and all the commit logs. After this, I will try to make this game 3d, because it will be better in the long run.


+ Today, it will only be posted to the game website, but tomorrow, maybe I will try to update the steam page as well.


+ Game build didn't work at first, which nearly gives me a panic attack that the GamePrefabDatabase refactor wouldn't work (because it use Just-in-time type checking, not pre-compiled) so it might not work. Turn out, the data was wrong, like, because I build the game, on this computer before, there are old save data that will not work with the new code (Json fields with different names). Clearing the saved data works. Nearly give me a huge disaapointment :p.


+ Finally fix the typo of the game name, from WhatThoPho to correctly WhatThePho


+ Yeah, I think I want to switch this game from 2d to 3d. It's a huge task to be sure to change so many things, but it will make this game more beautiful (because my 2d art skill are crap anyway), so at least with 3d, I can buy models and with correct shader, everything is a bit more same-styled. Also, 3d can fix a lot of problem that I have with 2d, mostly the rendering layer, order in layer, and probably also the position picking that feel super ir-responsive now.



-----------------------
### Sat Sep 12 00:56:05 2020 +0300



### [3hr]Finally fix the bug with the progress bar and food processor automatically get food from the spawner if placed on top of a spawner.


+ This bug caused by placing the object on top of the "stove" will call the set rendering offset function twice. This only happens on load because of the delay init function. I added a duct-tape fix to call onObjectPlaced on stove 0.2second after init, because there is a bug of, if a pot is load with scene right on top of the stove, the pot will not register as is on top of the stove, and if you put food in, it won't be cooked. I fix the rendering-offset bug now though.


The processor automatically get ingredient and process it if placed on top of a spawner.  Still, if you get food in it while it's processing, it will remain unprocessed with 0% progression. Simple fix by just not allowing the player to take already processing from the processor. It kind of makes sense to not be able to take from it though, so I think it's cool. Also, I'm tired with this processor now, so tomorrow I want to do another thing.


+ Add a delegateUtils file, so I can dump all the delegate definition there. It's cleaner that way.


+ Fuck, I started coding at 9, and now it's 1, but it doesn't feel like I did much. I did fuck around a lot, like, going to toilet, playing piano, and playing Clash Royale but I didn't mess around too much though. Probably because of thing just didn't work right away and I have to track down problems and fix it so that the processor works. Code is short but it took a while to write these short code.



-----------------------
### Fri Sep 11 00:48:31 2020 +0300



### [1.5hr]Refactor the rendering component a bit so everything is cleaner. The food processor works, but still ugly.


+ Refactor the progress-bar so its relation (inheritant) from rendering component make more sense and reduce more code.


+ Make the sub-renderer as a property of the rendering component for easier set-world off-set function


+ Make the WorldPopup inherit from the rendering component too because it makes more sense that way.


+ Don't use the sub-renderer in the processing but use world popup now. It's more visible that ways, and both looks ugly anyway, so at least I choose the ugly but more visible.


+ Add animation, but the animation I made look disgusting.


+ Plan to make the Food-processor automatically pick up ingredient and process if is placed on top of a spawner.



-----------------------
### Thu Sep 10 00:31:06 2020 +0300



### [30min]Add the Sub-renderer to the Processor component, so it will display what is being processed instead of the popup.


+ But this also looks a bit ugly though.


+ Small code update to use my helpers function (GetComponent and check null automatically) so sorter and cleaner code.


+ There is a bug with the SubRenderer, bascially, if things are put on top of table, it will be move back by some rendering offset to make the feel of 3d. This doesn't updat the subrenerer information though, so this should be fix.


+ I'm thinking of maybe making the sub-rendrer as an optional part of the RenderingComponent?



-----------------------
### Mon Sep 7 00:44:47 2020 +0300



### [2hr]Food processor work like 70%. You can put raw ingredient in, it will process it, and you can grad chopped food from it.


+ Now, if the object is under transition, if you remove it, you will just get a 0% progression object. I will fix it tomorrow.


+ No animation yet whatsoever for the food processor eventhough I spent hour making animation for it.


+ The position of the Object popup and the progress bar is really not optimal. I will need to change later.


+ Took some times because I procrastinate (I started working at 9, and in 4 hour, I got like 2 hours of work done, and that's generous).


+ Also because of some stupid naming I made long ago with the ingredient object. Transition Progress is just the total time, not the percentage transition, I spend a lot of time stucked there. Luckily, I have good debug skill (lol).


+ Also, more fix/refactor with the Move all Progress bar and Object Popup from specific prefab (Chopping Board, Stove) to all world object. Turns out my last refactor wasn't that thorough, so I finished what I should have done long ago


+ I have a half can of beer at 11.30, that's why this commit message is a bit long.



-----------------------
### Sun Sep 6 00:41:45 2020 +0300



### [1hr]Refactor the game prefab database.


So it's a bit smarter and not contains like 10 copy/pasted GetComponent function for every different prefab type I have in the game. So now, I have everything in a Dictionary<System.Type, PrefabType> that can lookup from it, and I can call the GetComponent(System.Type). It's a bit weird because I thought system.type is like, pre-compiled, but seems like it's a thing that generated at the final step of compilation, so I can't use Generic type like function<T> or switch :/


Kind of feeling there are still better way to do it, and I am just playing with the coding syntax, but this is quite briliant already and I will try to make the food processor working tomorrow.



-----------------------
### Sat Sep 5 20:01:48 2020 +0300



### [1hr]Add the Processor prefab to the game, that can be easily spawn and remove. So, need to change in 3 file, which is a bit too complicated for my taste.



-----------------------
### Sat Sep 5 00:37:09 2020 +0300



### [1hr]Add animation and prefab for the Processor component.



-----------------------
### Fri Sep 4 00:20:43 2020 +0300



### [30min]Add art sprite for the food processor. This is a component that will automatically process food for you, from RAW to PROCESSED.


There will be two version of this.


+ One is that will just there and if you drop food on it, after a while, it will become processed.


+ The other is that if you drop it on TOP of a food container, it will automatically get food from the container, and process it, so all you have to do is to just pick the food up.



-----------------------
### Wed Sep 2 00:43:29 2020 +0300



### [3hr]Add the processing ingredient code, also make progress-bar appear on processing ingredient.


+ Problem is that my processing object art is super ugly and you really can't tell that if the food is under processing or not, so let's just use the good old progress bar.


+ I could probably improve the art, but this will be a task of distant future.



-----------------------
### Tue Sep 1 00:41:43 2020 +0300



### [2hr]Add processing sprite for ingredients, and update the json data format.


No code update though. The ingredients updated are Beef, Chiken, Tofu and MixVegetable. Also change the art of the chicken-processed.



-----------------------
### Sun Aug 30 23:44:37 2020 +0300



### [Hot-fix]Because I just found a new bug/improvement.


+ Right now, the ingredient, when being chopped, will have a progress-bar show up, but if they are picked up, their progress-bar will be hidden, which will be confusing for the player. Idea are either make processing ingredient always have their progress bar show up and/or have a sprite for ingredient that is in the processing phase (which is also helpful anyway).


+ Fix the map_0, make it bigger, I feel a bit too crampped playing in that map.



-----------------------
### Sun Aug 30 23:37:37 2020 +0300



### [1hr]Did the TODO from friday I think.


+ Fix the bugs related to content transfer between cooking pots. My food-recipe-interaction code is, well, confusing so I renamed a bit, so it's shorter, so it's at least easier to read.


+ So, transfer between cooking pot is two ways now.


+ Wife is going to sleep early today so I will also go to sleep early. Next week, I will create more content,


+ For example:


- cooking pot that will be burn if overcooked: Require code change in recipe json data, new art and some code.


- queueing customer: could use the same art but will need new customer class, that is interactable


- a dish/bowl/cooking pot rack: new art would be better, code would be simple though because I already have container code.


- Ingredient food will have limited value and will have to re-buy? This will create more depth as the player can buy more premium quality food to make better food, but might be confusing.


- Automatic dish-washer: new art, code wouldn't be too hard.


- Automatic ingredient slicer/processer: Basically, you put this on top of a ingredient container, it will get ingredient from there and process it, so you don't have to chop meat anymore.



-----------------------
### Sun Aug 30 00:47:17 2020 +0300



### [30min]No code with this commit, just had an idea in the morning and I should write it down as a GDD (Game design document).


+ One core idea of a rogue-like is that you progress through the game with a health-bar that act as your main currency. If you run out of health, you die, and every encounter, you have to trade some of your health with the enemy to gain better loot/gold, etc... In this game, there are no way to make a persistent health value from one day (round) to the next day (round) yet. So, if every-day is the same, the player just play to gain more money and beat the high-score, it's just a level climbing game, not rogue-like, especially that the target everyday is more or less the same, survive all the customer and gain as much money as possible.


+ So idea is that every day will has a "Rating score". Basically, if you successfully serve a customer, he/she will vote the restaurant positively (5 stars, maybe), or if bad, he will rate negatively (like 1 star), so if the whole day, the Rating drop below a certain number (40/100), maybe, he will automatically lose.


+ The score, while is consistent, will be day specific, and total rating will be the average value.


+ For example: Day 1: Rating 60/100, day 2: 70/100, day 3: 40/100 -> The average score will be 170/3 = 63.33. So, if the average rating falls too low (like 50/100) calculate after day ends, he will lose. This might be too harsh though as when the player complete a day, if the screen says he lose, it will feel bad. But, for example, player start the first day with, for example: 70/100 base rating, and then, each customer rating will improve/decrese that value. And the "starting" rating of the next day, will be the total average of the whole week, which give the whole week rating some meaning.


+ Another idea is that as the days in the week progress, the minimum required rating will increase, but this might leads to also case of when day ends, player realized that he loses, which isn't fun. So maybe idea is that if a new day has a new higher rating than the player has, like 60/100, but player only has 40, he will enter a grace period of 1 minutes, that if he doesn't increase his rating, he will lose. This grace period can apply to normal calculation as well, maybe.


+ Also, idea for higher ascension is that if player serve customer quickly, they will reward better rating, and if serve poorly, maybe neutral rating or just bad rating.


----------


+ Another idea of rogue-like is that you should be able to choose your own path. This is well, difficult as this is not a dungeon crawler, but we could have it like:


-> The game runs in the course of 4 in game weeks, where at the end of each weeks, you enter a boss-fight phase or something similar. So, one "Act" runs from Monday -> Sunday and if you don't lose, you enter the next "Act"


-> As the week progress, there might be some free-form days, where, for example, Wednesday, where player can choose to go for some event to earn some special rewards, for example a "FAVOR" with the judge or the seller that will give some advantages, but sacrifies one opening day, so he won't earn more money from restaurant, and maybe risk losing rating (because closed restaurant is bad.).


-> Maybe player can has side-quest each day, and if he accepts, he will earn "favor" one time value (like potion works in slay the spire) or special gadgets (like relic in slay the spire). Favor sounds cool, like, let the player borrow super cooker for one day, or like, an auto cleaning robot for 1 day. Max 3 favors at a time, maybe.


-> As the restaurant open on evening, maybe we can make it like, player can choose what to do in the morning. So, either prepare/clean/re-arrange the restaurant in the morning, and ready for the openning, or skip morning to sleep/rest (happier, so maybe like, faster or smile more so customer are happier?), things like that, like persona but not as detailed. This will add a small layer of decision making for the player, as if he wants to go to an event or spend time and clean-up the mess that he calls a restaurant.


---------


+ I'm thinking of also putting the pattern of number of customer fully shown to the player. So like, openning from 7pm -> 11pm, And peak customer at 7.30 and 10.30, so like, at that time, there will be 3 times the customer as usual, and show that info to the player, so he can make the decision better.


+ Or better yet, that calendar info can be a relic/gadget that the player must sacrify one openning day or one morning to go to.



-----------------------
### Fri Aug 28 00:12:02 2020 +0300



### [2hr]Fix bug with Buy-Sell-UI, add feature to pour content (food) from one POT to another POT.


1. The buy-sell-ui will not close itself after buying stuffs. This was left over interaction when I copy the resume button to the buy menu, I think, or I just intented it to happen at the first.


2. I can pour food (content) from one pot to another now, which is nice things, also, some refactor with some food-container related functions so the naming can be understand clearer (I hope), few things left though:


TODO:


+ Bugs fix: If one pot is completely added (full recipe) and fully cooked, it will return an error. Both case, as, get from pot on table to hand, and the other way of pour from pot on hand to pot on table. Those are 2 different bugs though


+ Maybe make it possible to Get content from pot on table to pot on hand. Currently, this is only one way interaction. From hand to table only, not the other way around. It's possible to get food content from Cooking Pot to Bowl this way, so I guess it makes sense, and consistency sake to make it possible to do from Pot to Pot, both way.



-----------------------
### Thu Aug 27 00:39:32 2020 +0300



### [2hr]Bug fixes and proper test with the day summaries so I think it work well now. Next will fix bugs and add features.


+ The RT + LT to speed-up is implemented (it was just commented out).


+ Another improvements to the game is that if you have an empty cookiing pot (presumably on a stove), you should be able to pour the content (and the progress) of another cooking pot into it.



-----------------------
### Wed Aug 26 00:33:28 2020 +0300



### [1hr]The end day summary works now + find some new bugs and some new ideas.


+ If you don't have enough score. It will say you lose and prompt a game restart. If you have enough, you can go to next day. If it's the final day, there will be a you win show up and a restart button.


Bugs:


+ The first cooking pot on the stove, when putting stuff it, the progress bar is way too high for some reason. If you pick it up and drop it, the position is set to normal, but no idea how that happen or how to fix. Note: this doesn't happen when I buy a new stove and buy a cooking pot so that it spawn on the stove. Only the one appears when you load the scene. (Not really load the scene as the object managers delete everything and spawn from save files)


+ When loading restaurant layout. It's super bugger. It should be fix because it means my code has holes, but it will not be in the final feature though.


Improvement;


+ press RT + LT so speed up the time, and release to make time normal, so that debugging/testing is faster.


+ making collider of object more round. RIght now, it's a box and if you just stuck on to it, you stuck. Maybe make that it's circle so if you stump on it, you just move a bit slower, so the game feels better.



-----------------------
### Mon Aug 24 23:53:13 2020 +0300



### [1hr]Fix bug related to the Day Summary not working, due to calling the Wait for second function while setting time scale to 0 due to pausing game (Fix by using WaitForRealTime). Also, add a small function to check if winning and losing game, so I will create a final winning game menu as well as a losing/restart game scene.



-----------------------
### Fri Aug 21 00:49:03 2020 +0300



### [2hr]Continue to work with the DaySummary, it almost works. Like


It shows up and has a button, but pressing it doesn't work (go to next day, hide the menu), and the text is not updated (not sure why).


Code looks all over the place and ugly. I don't like it, but this is like, test code so I will change later? Atlest to be a part of Doozy UI, and this will probably be something bigger.


Update the Unity config so that the director will always be called first.


Remove all reference to the number scroller. Such a waste of time, but I think it's because I was really un-focus in making the game and just playing mobile phones, until I realized it's mid night and I need to do something for the game. So yeah, my fault.


I really should un-install all mobile games.



-----------------------
### Thu Aug 20 00:16:08 2020 +0300



### [1.5hr]Draft of the DaySummary UI. It will display the day information to the player, and a button to advance to the next day. The number scrolling yesterday was a bad idea, not "bad" idea but like, the implementation idea of mine was bad. It should not be a helper non-mono class. Should be a full on class and other things can call upon it.



-----------------------
### Wed Aug 19 00:50:32 2020 +0300



### [1hr]I was trying to create a UI display so that it can display all the important game information after a day, then I got side tracked and create a number scrolling (running, animation) and it didn't work (yet). Feel kind of pointless and idiot for focusing on such a small detail instead of prototype the game now. Also, feel extra useless for wasting time playing stupid video game (Toon Blast, really addicting casual game).



-----------------------
### Sun Aug 16 23:58:33 2020 +0300



### [1hr]Add a on restaurant phase changed delegate and some small fix. I was really un-productive this week.



-----------------------
### Tue Aug 11 00:17:08 2020 +0300



### [2hr]Add a debug helper so I can just add some test/clean-up script to put there and use in editor (for example, one to clear all the player-prefs). Also, add a Restaurant-phase, so now, it will have 4 phase (prepare/openning/closing/ending) instead of just open/close like before.



-----------------------
### Tue Aug 4 00:24:13 2020 +0300



### [2hr]Fix the bug I found yesterday, and add a simple score counting, so that the player will have to play better everyday to get the good score to pass until the next day.


+ The bug yesterday was fixed because I was really silly, I didn't add the customer in the queue to the current custoemr list, thus, their update function is never called, thus, the table will just show them up at X and they will never run their timer. So they will never leave, and even if you serve them food, they will just eat forever.



-----------------------
### Sun Aug 2 23:54:41 2020 +0300



### [3hr]Add the game announcement to announce important information to the player. Right now, to just annouce like 60 second left, 30 second left, or things like that.


There seem to be a new bug of customer timer not working again, probably due to my refactor or something, will try to fix tomorrow.



-----------------------
### Thu Jul 30 23:56:06 2020 +0300



### [0.5hr]Try to fix the map preview but couldn't, so just change the door preview from space to "," symbol. Weird bug. Also, slightly optimize it using StringBuilder instead of just string, but this weirdly doesn't fix the bug.


Also, will probably work on a big UI show up in the middle of the screen, like big announcement of such.



-----------------------
### Thu Jul 30 00:21:14 2020 +0300





*Quick bug report* Something wrong with the map preview in the game menu, that it somehow display the MAP_2 all wrong. However, it only display wrong if I add the door (D) character to the map, if I let it as wall, everything is good. Just a string replace (d to space) why it didn't work?



-----------------------
### Thu Jul 30 00:17:45 2020 +0300



### [2hr]The default map layout saved by the user. Is now implemented. Next, I would want to have score, game over state and things like that. Right now, just increase the target score everyday, and then have the player try to reach that score.



-----------------------
### Wed Jul 29 00:11:59 2020 +0300



### [1hr]Fix the scoring so that it works now. When customer finish their meals, this will increase score and money, and if it fails, it will reduce some score. Will make a scoring system and ways to auto save restaurant layout next. As well as idea for having customer enter and queue from the door.


Both bugs I noted down yesterday were magically disappear this morning when I open the game and check again. Probably because of either Unity editor or my computer issue



-----------------------
### Mon Jul 27 23:52:12 2020 +0300



### [2hr]Big huge refactor. Add the Popup and the Progress bar to all objects in the game. This is to make things a bit more streamlined and things more flexible in the future. This will come with some performance, I guess, but this is a pixel game, and these extra component each will eat probably a few kb of ram, should not be any problem.


Also, there are two bugs I need to fix immediately now:


+ First, when the customer finish eating, if you pick up the bowl, there will be a null-reference. This is due to a refactor with customer/dining-table I made on Saturday.


+ Second, somehow during this time, the controller can't navigate the UI anymore, both the UI, main-menu and everything. No idea why, hopefully, when I turn on the game tomorrow, it will magically work again.



-----------------------
### Sat Jul 25 19:42:10 2020 +0300



### [4hr]Commit after another long period of procrastination. :(  FIx bug with restaurant closing that will cause all customer logic to not update.Also, refactor the restaurant opening timer a bit so it's in the restaurant manager, not in the ui component, lol



-----------------------
### Sat Jul 4 01:17:49 2020 +0300



### [2hr]Finally fix the bug that cause pre-placed cooking pot on stove are not recognized unless you pick it up and drop it again. Due to map initiazlization.


Also, fix bug that make us somehow able to serve customer un-finished food (like, bowl of beef without vegetable).


Next, I will move all the world-display/popup/progress-bar as part of normal world object, so it will apply to all, not "just" some special object anymore.


Also, I want to fix the pick/drop targeting system so it feels better to play.


Finally, I want to have some better visual feedback on various item, like, stove cooking, customer eating...



-----------------------
### Fri Jul 3 00:34:57 2020 +0300



### [3hr]Finally the Dining table and Game customer refactor is done. It works like before, hopefully, so the code is still a bit messy and I have a dread feeling of bugs in here and there, but it's finally done, so I will try to finally work on the game. I have been super procrastinating, so hopefully, I can be more serious this time.



-----------------------
### Wed Jul 1 00:18:07 2020 +0300



### [3hr]More work with the dining table and customer. It almost works, some bug/error when customer leave meal only.


Another long procrastination, ahh, damn it. Finally learn to set a timer limit on my phone so that I won't browse too much reddit and facebook (so, 15 mins combined daily).Hopefully, this timer will help.


Also, another reason is that we went on a small summer trip to a summer cabin in Kuopio (finland) so, it took like 4 days, and after that, I spend the rest of time finising "The Outer Wilds". It's an amazing experience, 10/10 recommendation. Also, just bought a new 55 inches tv, so it's also another distraction. now. Needs more testing though. Also, fixes on other part of the code, like the progress bar component, finally fix the long running bug that the progress bar somehow render on top of the clock/warning sign sprite (it's weird bug because of Unity).


Anyway, I think most bugs I fix today is mostly "work-around" the implementation of Unity. Fun time though.



-----------------------
### Fri Jun 19 23:59:09 2020 +0300



### [4hr]More work with the customer manager and dining table. It generate customer, add to a dining table if there are empty one or add to a queue list. With proper timer set up and everything.


Here, it said 4 hr, for today, but probably in the span of a whole week. I always open the project and the IDE, but never write down some code, or very little code. And even today, I set my goal to spend whole day (minus daily task) to do thing, I have the whole day off, and I didn't manage to do much. Really considering just delete reddit from my life :(



-----------------------
### Tue Jun 9 00:47:42 2020 +0300



### [2hr]Slowly rework the restaurant manager and dining table component. It's getting together, hopefully.



-----------------------
### Mon Jun 8 00:27:52 2020 +0300



### [2hr]Continue with the customer refactoring. Changed my mind (actually, found a better way of implementation) in the middle of the way 2 times already. Atleast, everything compile now, but that's because I deleted everything. Hopefully, it mights work tomorrow.



-----------------------
### Sun Jun 7 00:38:56 2020 +0300



### [4hr]After soo many delay (and I moved my home last week, which was quite stressful), I finally get down to refactor the DiningTableComponent code so that it's good to work forward. Right now,it's super WIP and there are compile error everywhere. Hopefully, I could get it working tomorrow.



-----------------------
### Wed May 27 00:13:11 2020 +0300



### [2hr]Trying to refactor the DiningTableComponent by adding the RestaurantManager class. Right now, each table handles its own customer task and count down. This is just a duct tape fix to trying to make thing work and test the water. Making a proper restaurant manager, and tasks giver for the player is the proper way to go. It's just a bit complicated. Heh


Another long break, because I played Xcom 2 (and finish it) and watched Barry season 1 and 2 with my wife.



-----------------------
### Mon May 11 12:47:33 2020 +0300



### [1hr]Art fix. Update the sprites of table and diner table so that it looks slight better.


Change the Computer prefab so that it also contains a table sprite, as it is now a computer and a table, and will take place in both layer (ground and top). So we can arrange stuffs a bit easier, and more intuitive.



-----------------------
### Sun May 10 21:28:49 2020 +0300



### [2hr]Try to adjust our food data so that we can add vegetable to empty bowl because that's what I noticed a lot of our user did. Then figure out another nasty bug that gone completely through because the code never reach that part.


Also, make it that press [Y] (pick up heavy stuffs) will also pick up small stuff if there is no valid heavy stuffs.


Kind of want to refactor the food/recipe thing now. I think I have a better way of making it, but well, it's still work, so I think I should not touch it too much.



-----------------------
### Sun May 10 16:50:31 2020 +0300



### [2hr]Fix bugs that make objects not saved properly with the new set up. Also, rework with the ingredient spawner a bit, so that it's more consistent with the way other class is set up, so that their values is setup first, and then we call the init function.


Find out some weird bug:


1. If you buy a Sink/Stove, and then buy another bowl/cooking pot: the cooking pot/bowl will be spawn on top of that. It shouldn't happen.


2. If you save a layout, load it, and then load again (that layout or another layout) It will have a despawning error from the grid manager. I'm too lazy to fix it now, but it must be fixed.


3. I should also should create a test class, to validate all of our data.



-----------------------
### Sun May 10 01:31:40 2020 +0300



### [4hr]More work with the GamePrefabData update. So, I fix all the bugs yesterday and manager to make everything working again. Then, I add more update, because it's needed, and now everything is not working again, but it should be finished tomorrow.


This is just mostly repacking data so that it's more convenience to pass data around and less error prone. Now, it dawns on me that I have 4-5 json data files, that is so inter-connected with each other, such that if I change one value in one file, all the other file would stop working, and because they are all text in json file, no compiler can help me catch them. Which, leads me to the needs of another test system.


Due to this refactor, I figured out another bug I made when I was creating the savable thing. Somehow it went all over the rader for 2 months, until this refactor.


I fixed a bug with Trashbin stop working due to another refactor as well.


This is becoming really tiring and I need an automated test system, so that I know that whenever I made a new change, old thing still works. Because all of this going in back and forth cost a lot of time, not just going back and testing if shit works, but just the process of testing is also time consuming. If I can make an automated test system that can just test everything, so I can make new features, press a button and know that all the old stuff still works, that would be really nice.


TL;DR: unit tests and integration tests.



-----------------------
### Fri May 8 00:56:17 2020 +0300



### [1.5hr]More of the refactor of the GamePrefabData thing. Now that I also refactor the save-load-data mechanism, so it doesn't work now.


Somehow, the FoodContainer (Bowl/CookingPot) completely disappear in the scene and seem to be null, which should not happen for some reason. Will fix tomorrow or some day.



-----------------------
### Tue May 5 01:08:50 2020 +0300



### [2hr]The buy menu layout work in a way that it can now automatically spawn the menu grid based on the contents inside the GamePrefabData config file.


Next is refactoring the spawning system and make the sell button works.


After selling work, probably some refactoring with the money/score/dining-table system because I wrote it in a rush for the demo.



-----------------------
### Thu Apr 30 00:45:20 2020 +0300



### [1hr]More work with the GamePrefabsData class. It now remove all the old uses of "string" reference from Unity Editor Game Object name, which is not good.


Find out some bugs with the SaveLoad functionalities, probably because I rewrote many save load code. But, it shouldn't happen. It might be because of my refactor, or it might related to the object in ANY layer stuffs. I don't know. Must test tomorrow.


Now, I think that I should read more about Unity Automated test, and create some unittest, so that whenever I create a new feature or refactor something, I know that it works and doesn't break something else.



-----------------------
### Wed Apr 29 00:33:17 2020 +0300



### [1hr]Adding grid layout to the buy sell menu. Will try to make it dynamic. Also, more base work with the GameItem/Prefab manager.





Hopefully, I can get a working prefab database system by the end of this week. This will be in charge of reading and serializing data. Also handle the data thing, like spawn rate, price and such.



-----------------------
### Mon Apr 20 00:36:44 2020 +0300



### [10mins]Check for some TODOs and remove I think like 2 or 3 of them. (Total now: 21)


It's nice that I have Todos commented in the code, and all of them seems descriptive enough that I do have solution for. Now, I do wonder if I have some thing missing that needs to be done. Let's hope I don't have that and have the discipline to always add more todo to the code. For the record. I now have 21 todos in the code.



-----------------------
### Mon Apr 20 00:28:45 2020 +0300



### [1hr]Trying to work with the new GameItemData thing, ended up remove a lot of code, which is good.


The idea is that that I will have a single json file that keep information of all game prefab (which I change the game item data name to game prefab data. Which, will handle stuffs like, cost of items and rarity and other stuffs like that as well. Ended up find out about some code I have written long ago that should be removed: Such as PickableData, or Container Component (mostly remove codes, because this use PickableData extensively).



-----------------------
### Sun Apr 19 14:27:31 2020 +0300



### [2hr]Remove the FoodContainerSpawner component. Make the KitchenSink (the one to clean dishes) to a locking interactable objec.Fix a bug with the ANY layout world object.


+ Remove FoodContainerSpawner: Includes the script, the prefabs, other reference to it in the buy/sell/spawn in the object manager And remove it from the saved layouts.


+ IsLockingObject is a properly that tell if the interactable object will LOCK the player to the object (you can't do anything else, unless you press B to cancel the interaction). This will make it similar to the chopping board, as if you press X more, it will speed up the process, but if you don't do anything, it will clean the dish, just a bit slower.


+ There is a bug with the object that can be dropped to ANY layer that if you drop it to the ground, it will act as a table. Which shouldn't happen. Fix that so that if you place it on the ground, it will occupy both ground and top layer.



-----------------------
### Sun Apr 19 01:15:05 2020 +0300



### [1.5hr]Create a GameItem data json file and class loader. This json config file will be used as our whole database for all item in the game, as well as their rarity and cost.





The data file is here and I'm done with the data structure. Will work on the loading next. I will try to remove the FoodContainer Spawner soon and rework the SavableData object a bit, as it's really similar to this GameItemJson.



-----------------------
### Sat Apr 18 00:39:35 2020 +0300



### [1hr]Add the AnyLayer to World object, which make it possible for us to have a object that can be place either directly on the ground or on a table. Which I now it for food container object (Bowl, Cooking Pot), so that I can remove the stupid FoodContainer spawner thing, and buy a bowl directly, not like, buy a bowl, but you buy a box that have a bowl inside and you can use it as a table as well.



-----------------------
### Wed Apr 15 00:44:26 2020 +0300



### [2hr]The sell button works halfway. Remove some useless UI-Code about the buy/sell menu. Refactor the Object manager despawn function so it works properly top down.


+ The sell button now can detect all objects in the recycle zone and remove it. Nothing to do with money yet because we don't have a Money Manager class yet. Next is to work on a money manager class.


+ The Despawn function used to be in each Object itself, and when called, it remove itself and report back (update the object list) in the object manager. Now, it works that the object-manager call the despawn function, and remove from its list. So slightly better.


+ Need some refactor with the Pause Menu I think, I can remove the PauseMenu class, it's useless. Generally, my UI is quite mess up (I think all projects UI code is messed up).


+ Add a ANY cell state, idea is that an object can be placed either at the ground, or on top of a table. It used to be JUST ground, or Just table, or BOTH. This work for, bowl or pot for example. So now when people buy a bowl or pot, they just buy a bowl or pot, not a table contain a bowl, or a pot. Really useless.


+ Make the Computer so that it is a table with computer, and it takes both layer at once. Right now, the computer is a table-top object, and I think it's confusing to have to move the computer. Press A with the computer should probably interact with it as well.


+ Make a sprite/state for a bowl with lectute on it. Players from testing (even me) always want to chop vegetable, put it in the bowl, but couldn't do it. I think it's dumb. So, more sprite.



-----------------------
### Mon Apr 13 15:29:56 2020 +0300



### [2hr]Add the default layout setup for each map. Also, fix some bug with the UI and a bug related to the computer prefab missing the computer script component.


map_1 is quite ugly and not really well functioning, so I think that should be remade. Also, will need a working selling button on the Computer (shouldn't be too hard to make I think), and some sort of guidance or tutorial.



-----------------------
### Mon Apr 13 00:44:09 2020 +0300



### [30min]Rework map loader a bit so that it's not a duct-tape add on anymore. Next, will try to make a default layout for each map.



-----------------------
### Sat Apr 11 15:22:21 2020 +0300



### [2hr]Fix the bug with the UIs that if you navigate between different UI view, and moving the joystick while the ui is transitioning, will make the button not selected, thus, hard lock the player out of the game.


I'm really glad to fix this, because it's been annoying me quite a bit about the game and I though that it would took forever to fix. It's not the "fix/fix" to the solution, but rather a duct-tape fix, in that I will have to make the UI behave in some certain way, but it is fine and I guess I will just have to live with it.



-----------------------
### Tue Apr 7 23:36:34 2020 +0300



### [30min]Not doing much, but hopefully this will get me back on track. Trying to fix the UI and fix the compile error I made the other days.





The start-menu now can be controlled by controller now (previously, it was only controllable using mouse, which make demo-ing really awkward. Anyway, next is I will try to make a default layout for each map. So that each map will have a at least passable layout.



-----------------------
### Mon Apr 6 00:22:15 2020 +0300



### [1hr]Moving some ui files around. Hopefully, this time I will get the discipline to work.

