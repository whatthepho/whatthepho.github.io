---
post_time: "14th Dec 2020:"
title: "Sixth update. Toon shader, Unity URP and Antiliasing. Also, UI refactor"
excerpt: "2020-12-14 - Progress update"
toc: true
layout: posts
feature_image_path: "/assets/2020-12-14/serving.gif"
---

+ I finished with the Toon shader and the Unity URP on 30th Nov 2020 (lol, that was half a month ago already). Then I found out that like, most of my UI doesn't work anymore. Which, I have to refactor the whole UI thing, by removing the UI library, and recode most of it. It still has some bug at this moment, and there is no animation so it feels really dry, but it works I guess.

+ Toon shader, looks great (I think), still, it feels a bit too gloomy, which I want the color to pop up a bit more, like, more cheering. But probably that is the work of post processing color correction/tone-mapping?.

+ I really just want this to be done, like, finish this relesae so I will finally add more feature to the game.

+ I seems to be procrastinating a lot recently. But this seems to be a trend, like I would have one quite productive week, then one (or two) really crappy week, and so on. Really hope I can improve the situation.

+ Anyway, here the progress. Absolutely chaos!

![image.png](/assets/2020-12-14/chaos.gif)

+ Serving and multitasking!

![image_2.png](/assets/2020-12-14/serving.gif)

+ Some organizing at the restaurant.

![image_3.png](/assets/2020-12-14/buying.gif)

-----------------------
-----------------------
### Thu Dec 10 00:56:00 2020 +0200



### [1hr]Fix the bug with the UI. Remove all Tween animation.


+ The UI is fix but still quite cubersome though.Because everytime the back/exit button is pressed, I have to call the DeactiveUI function manually to set the timescale back to 1. I think maybe adding a delegate or Unity function and subcribe all the resume button to that would be nicer?. Maybe.



-----------------------
### Mon Dec 7 01:00:21 2020 +0200



### [1.5h]Update day summary code so that it works again and refactor it a bit too so that it's better.


+ There's still some hole in the UI, but I will do more testing tomorrow, and probably remove all the annoying warning in the unity console too. I have like 30+ warning now, which is a bit annoying.


+ Hopefully next week, I am able to create a new release (lol, just blog post). I was planning to do a new relese last week, but then after I build the game, and found out that UI didn't work and then I have to refactor the UI, which took quite some times (mostly because I was procrastinating a lot).


+ I uninstall BanG Dreams from my phone (decent music game, just the Gacha and monetization kills it) and decided to install Honkai Impact 3rd, same game from the Genshin Impact developer to scratch my Gacha itch (gacha addiction is real lol). Played for like 30 mins, feel guilty, comes back to develop game and spend like more than 1 hour reading reddit/r/genshin_impact. At least I still was able to do some work, but I really shouldn't un-block reddit for today, lol



-----------------------
### Sun Dec 6 17:29:49 2020 +0200



### [3hr]UI now works except the end-of-day report. BuySellMenu also works. Lot's of refactor/restructuring with the UI.    + Fix the bug yesterday where the controller just doesn't interact with the UI. Turn out, I was missing the EventSystem for UI.


+ Buy Sell menu works, and ofcourse some restructure to make the code shorter/esily readable.


+ Make the UI interaction better, pressing Menu/B button is now universal to exit all the UI.


+ Found a bug that if I place the FoodProcessor on top of the BanhPho/Noodle spawner (non-process-able food), it will spawn a BanhPho in the middle of the map.



-----------------------
### Sun Dec 6 01:16:18 2020 +0200



### [1hr]Refactor the PauseMenu View in the base game a little bit - remove a lot of work-round needed because I was working with Doozy.


+ Fix some UI flag so that at least we can play the game normally. There is this boolean to check if UI is active then our player will not takes input anymore.


+ The Main Pause Menu view works now. As in, if I press start, it does show up, but now it doesn't interact with the Controller button (yet).


+ Also, remove some functionalities, like I used to have multiple save/load layout but I decided to remove them all and just have 3 buttons now: Resume, save layout as default, and exit to menu.


+ Update text mesh pro so that it doesn't print thousands of logs about some thing that clearly doesn't happen.


+ I had from 10 until now which is 1:15, like 3 hours to actually develop and fix UI, but then I procrastinate soo much, like install new gacha game and test them (BanG Dream, nice music game, but gacha and stamina system make it soo annoying) and testing the water with Honkai Impact 3rd - same dev from Genshin Impact. And I was planning yesterday like, I was going to spend 5 hours today developing game, urgg.



-----------------------
### Sat Dec 5 22:19:30 2020 +0200



### [1.5h]Add Button Wrapper to make it easier for me to work with UI.


+ Create mostly shortcut function to change button text, add action listener and later on, if I want, make animation in here.


+ Remove UiUtilities, it's mostly the way I work around DoozyUI, now that I remove it, I just make my OWN UI wrapper.



-----------------------
### Sat Dec 5 01:02:21 2020 +0200



### [1hr]Fix the start menu scene.


+ It works again now, no cool effect though, which is a bit sad, but easy to make.


+ There seems to be a bug that, if I choose 2 players and enter the game, there are null rererence about player prefab, I should check it after I'm done with the UI fix.



-----------------------
### Fri Dec 4 01:05:51 2020 +0200



### [30min]Remove DoozyUI, first, because it doesn't work anymore, second, it's quite big, so getting rid of it was good. Nothing works now though. Will fix tomorrow.


+ First, Doozy doesn't work with new Unity (2020) or with URP, not sure, but it doesn't work, and I install it on a fresh project, and it has tons of compile error. Reviews on the web-store also state that the dev doesn't response to email (in 7 days, at least), so yeah, no reason to keep it.


+ So I assume that none of my UI will work at all, but well, just change the code from DoozyUI to native Unity UI code and it should be simple. I will lose some of the cool effect though. Luckily, I have bought DOTween PRO so it should be simple to make nice interactive AI.


+ Watched the movie El Camino: A breaking bad movie today. It's great. Like, it's a new movie, but everything feels just so nogalista, I love breaking bad a lot, and the movie was just perfect, captures everything I love about Breaking Bad, and is also an awesome movie on top of that. So yeah, was planning to fix UI today, but got side tracked by the movie. It's nice though, I haven't seen movie in qutie a while.


+ I am still playing Genshin Impact and will probably for quite a long time. I know it's a Gacha game which is bad and for the money I putted in the game, I could spend on like 3 AAA games, but the nice thing about Genshin is that, it actually limits my gaming time, like after 30mins-1h, I am done with the game, so I feel satisfied enough about gaming, and can focus on my work, not like, if I started like Hades, I will just spend the whole week playing it, or like Persona, that's like 1 full month of just NOT working in the game. I mean, yeah, of course, I can just NOT play game, but well, procrastination is strong, like, I am inclined to play at least some form of gaming, because else, I will just waste time on something else, so at least, with Genshin Impact, it has a clear limits and I can be more productive when I'm DONE with the game for the day.



-----------------------
### Mon Nov 30 23:40:09 2020 +0200



### [1hr]Shadow is fixed. My game now has proper shadows and it looks beautiful. UI doesn't work now though.


+ The RealToon dev is really good and responsive, easily 5* rating for me.


+ Figure out that my UI doesn't work now, probably because of the upgrade from unity 2019 -> 2020 and I don't bother to check the the UI, just check the game, lol



-----------------------
### Mon Nov 30 00:26:09 2020 +0200



### [2hr]Add some post processing. Figure out another problem with shader, heh


+ Only use the Anti-aliasing and very little color correction, as it feels quite nice already. I think if I want color change, I should tweak the shader and the color and art, the game is kind of fine as is now. I guess some color correction might be needed later in the future, but when I have a more clear-er feel of the game.


+ Tweak the shadow value of objects a bit, so the un-lit side will be slightly lit up (black from 1 to 0.65) so it's a more toony-look.


+ All of my objects doesn't cast shadow, this seems to be a problem with the shader config, after tweaking and reading the documents a while and can't solve it, I posted the question on the Unity forum, hopefully the author forgive my stupid mistake and answer my question.


+ There is a but that cause the objects to sometimes set to a really weird scale. This is probably because of the jelly animation I set on them, in addition to the scale up/down on target effect. I should remove the jelly/Tween animation to most object now, as I feel with 3d, I have more way to make object feel responsive now, like actual 3d animation or particle or something.



-----------------------
### Sun Nov 29 19:54:16 2020 +0200



### [2hr]Install the New Unity URP.


+ Don't know if it's some improvement or just my feeling after everything work, but things looks a bit better, color seems to be a bit brighter. Maybe it's true that something is change because I have to update the shader to the URP version as well, so it's different shader.


+ Re-organize my asset a bit so I can filter them/view them inside the Unity Package Manager better.


+ Found a weird bug like this:


Found a bug with the grid-high-light object. I have a velocity check that will only calculate the player cursor grid if the movement velocity is not 0. However, there is a bug that cause it to not register if we move directly UP or DOWN. We can test by looking right/left at some object: it get bigger -> Now, move down or up directly (using keyboard S/W) or the d-pad button on the xbox controller (joy-stick won't work as it's not 100% up/down). You can see that the object is not smaller. No idea what is the causes, probably the movement code? Disable the velocity check so that it check grid everyframe seems to fix the problem. Not a big issue though because the grid check is just x/y division so quite small, so it won't cause much performance issue.



-----------------------
### Fri Nov 27 23:35:10 2020 +0200



### [1hr]Update Unity from 2019.2f to 2020.1.14 (it's already the end of 2020 and it's still 2020.1 ???)


+ Update my packages because I have latest Unity now, including Doozy UI, DOTween and Rewire.


+ Will test more the game tomorrow and update to URP and add some neat post-process effect.



-----------------------
### Thu Nov 26 23:59:31 2020 +0200



### [30min]Reduce the outline of object from 2 width to 1, so it look less extreme.


+ Add the logo to the project setting.


+ Trying to install Unity 2020.1 (newest version) so that I can update the project to URP next, and have some cool post processing effect, like anti-aliasing and some color correction.



-----------------------
### Thu Nov 26 00:09:42 2020 +0200



### [1.5h]Fix the grid-high-light system. Move the camera much higher with an up-ward angle of 75 degree (from 45 degree). It has more top-down feeling, but much better visibility.


+ The grid-high-light system used to be a 2d square that is draw on top of whatever the player is targetting at. It's very subtle, only appears if the player hasn't move for 0.5s and the color is very subtle as well (light green with 55/255 transparency), so no one really notice it, even me, the def. So, this time, I make it a lot more aggressive. The player has a picker component that is in charge of deciding what to pick up and what not, so now everytime this picker target change, that object will be scale slightly up (from 1.0 to 1.1) so it's very clear feeling of what the player is looking at. I tried doing some animation like, pop an animation when the player look at something, but because animation have animation time, it's very confusing and the game looks crap, just a single pop up when in target and back to normal when not in target anymore is quite effective but not too much confusing/in-your-face.


+ Still, I still missed the drop/pick sometimes, especially when ordering new customer or givve food to customer. One idea may be that make the player even smaller and move slower, so everything around is bigger, thus, less sensitive to movement. Another way is to make the pick/drop component check. If it's empty,maybe check for other valid tiles in 4 other direction. maybe?



-----------------------
### Sun Nov 22 17:55:52 2020 +0200



### [1hr]Fix the placement of the top-up text in food processor and food container.


+ Fix the bug that make the background show on top of all text (due to sorting layer).


+ Resize the food processor, so that it now looks like a food processor, instead of a smoothy blender (well, its original model was a blender so ...)


+ Also, tried play the game a bit to get the feeling of it, it still feels really bad to play as the targetting system still sucks. I wonder should I fix the targetting/picking/dropping of everything first (this is part of the movement, right?) or I should make more content, for the MVP, like start with a calendar system, so the game will have like 1 full week of playing with clear goal, and like, making more items and upgrade. Like, similar to the food processor, now you should have dishwasher? And a cabinet that you can store item?


+ I think it's very important to have a MVP first, that's why I haven't even done the sound yet. I know sound is very important to have, as it also increase the responsive rate and everything, but it's like extra cream on top. If the game isn't good, having amazing sound won't help anything.



-----------------------
### Sun Nov 22 13:08:00 2020 +0200



### [1.5h]Update colors of furniture a little bit. Resize the text of the popup to auto size so it isn't too big.


+ Make the Warning icon on timer animate only, but now, it's a bit too big. I tried to fix it by updating the tweening code to consider the local scale but it doesn't work somehow. Now, just make the whole sprite smaller, but it's a bit crappy fix.



-----------------------
### Sat Nov 21 15:12:12 2020 +0200



### [2h]Resize all the prefabs/models a little bit so that on the game, they looks fitted together, and have some sort of grid feeling. Adjust the color a bit too.



-----------------------
### Sat Nov 21 00:41:12 2020 +0200



### [4hr]Adjust camera angle and lightning. Tweak shader a bit, add background, fix some bugs. Surfing at the asset store for more than I should.


+ The toon shader is really powerful with lots of options, I think I need like 1-2h with an empty project to JUST test it out, and read the manual as well, because I feel like eventhough the game looks better already, I feel like I still missing a lot of features to make it trully awesome.


+ Add another chair to the dining table so it looks like dining table, not classroom chair and table. Also change the color of the chair cushion from pink (same with table) to green to make it a bit stand-out.


+ Fix a bug that makes the customer would always seated to the tables in a order, which isn't nice. Make it so that they sit on random table order.


+ Found a bug that make the progressbar to NOT FACE THE camera properly.


-> To reproduce, just let the progress bar run one full course from normal -> timer -> danger -> done.


-> Then, the next time it appears, it will face to the wall, not to the camera.


-> The reason: this only happens when the DANGER bar shows up, if the progressbar hasn't run full course, it seems to be ok


-> This is because when entering DANGER phase, we run a DOTween set pulsing animation, which messes up with the rotation.


-> Just temporally disable the pulsing DANGER phase until I found a solution



-----------------------
### Fri Nov 20 00:17:01 2020 +0200



### [2hr]Bought a new toony shader and apply them to all the game assets. The game looks a bit uniform now, but the tiles and the models doesn't match. Also, fix the positioning of picking up object clip with the table.


+ Very nice that when I finally decided to buy the asset, Unity gives like a 50% store discount for like 700+ assets, which is nice. I might shop out for more assets. Heh



-----------------------
### Mon Nov 16 23:44:09 2020 +0200



### [1hr]Add the toon-colored shader to the materials of our food and some kitchen utensils. Next will be the furniture and some asset resizing and probably some light adjustment.



-----------------------
### Sun Nov 8 23:41:21 2020 +0200



### [30min]Raise the camera and its view angle to higher (from like 45 degree to 67.5 degree) so the game is more visible.


+ Add script to make sure that all the text/progress bar angled nicely with the new viewport. That code looks a bit convoluted, but still, I think I will redo all of them in the future.


+ Right now, when you take an object and move around, the object will rotate with you, and also the text on top also rotate, which looks funny. I can fix it, but I think it's quite funny to stay.


+ A weird bug appear that makes my controller unable to navigate around the menu. Weird because previous moment, it still works, but after I change some code, it doesn't work, but the keyboard still work. Re-starting the game doesn't help. This bug probably will be gone by tomorrow when I boot up the engine again. I guess this is either the unity bug or windows controller bug, or the controller lib (rewired) bug. Anyway, I don't care and I hope that it will disappear tomorrow when I turned it on again.