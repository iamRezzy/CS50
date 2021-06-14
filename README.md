# 50 Kart
#### Video Demo:  <https://www.youtube.com/watch?v=1S3B6ToDj8Y>
#### Description: 50 Kart is a game made using Unit and is based off of Mario Kart. The goal is to get through the checkpoints before the timer runs out! 

50 Kart is a game that I made using Unity and is based off the Mario Kart game theme/design. The goal of this game is to get through all the individual checkpoints before the timer runs out. Now this may sound quite simple enough, however it was not.

This project was made using Unity Game Engine 2020. This is a cross platform engine that was originally made to help users create and develop games themselves. The last four assignments in the Harvard CS50 Introduction to Game Design course happened to use Unity Game Engine. My familiarity and interest with this platform prompted me to use it for the final assignment as well.  Despite my eagerness and commitment to complete the project, I was faced with a big problem: I had no clue what to do to effectively start, nonetheless successfully complete my final project assignment.

As with any unfamiliar situation/challenge faced, I decided to use the resources available to me as part of this course. I am part of the CS50 Discord group server. So I asked others in the group for their input, ideas and suggestions on how to go about this project. Many members of the group suggested that I look at the Unity Game Engine 2020 as a first step. So, I explored the Unity Game Engine 2020 and found out that they teach you how to create a game that seemed quite similar/comparable to the Mario Kart game. The only difference between the two games, was that I did not add powerups, but I add checkpoints and a timer.  Fortunately, most of the in-game mechanics such as movement was already provided to the creator, which was helpful.

A focus of this project was to make the track challenging, (but not too challenging), to a point where the player is not able to get through the checkpoints in under 1 minute. All the in-game features, such as tracks, and obstacles are in the game engine itself. It is my responsibility to change game name, enable a timer, and make movement of the kart possible. To make all components of this game work accurately, I was given the Microgame project, which had most of the game files present. 

Now, I will explain step by step what I did to make this project work.

First, I downloaded the file and opened the Hierarchy window.

Next, I clicked on the “ObjectiveTimeLimit” GameObject and looked at the Inspector window. In this Mod, I used the Time Limit game mode. In the Microgame, the Objective scripts control the game mode logic, and can be configured to suit a variety of game modes.

The “Time Limit” game mode is controlled by the ObjectiveReachTargets component on the ObjectiveTimeLimitGameObject. I must click on it in the Hierarchy and then look at the Inspector window. Under “Objective Reach Targets” I must make sure the dropdown arrow is expanded and observe the field options.

Next, I went to the find Game Mode parameter, and set it to "Time Limit." Now that I have the Time Limit set, I need to make the game more challenging. So, I decided to create ramps. I need to set up ramps and move the checkpoints so that players must jump through them. To keep the scene clean, I created a parent GameObject under which we will keep the ramps. Then I right clicked in the Hierarchy and clicked on Create Empty. Another way to do this is to click on the "Create Empty" which will create a blank GameObject, which I can then add to the scene. Next, I right clicked on "Rename" and name it "Ramps."

Next, I went into Project View. I then dragged the "StuntJump" prefab into the Hierarchy onto the "Ramps." So not only will this put the ramp on the scene, but it will now also be much easier to move them around.

Next step is to add a Checkpoint. In the Project View, navigate to Assets > Karting > Prefabs > Props > Checkpoint. Next, I dragged the “Checkpoint” prefab into the Hierarchy into the “StuntJump” so that the new “Checkpoint” is a child of the ramp that it is for. The “Checkpoint” now inherits the transform properties of its parent, the “StuntJump”, so that when I move the “StuntJump”, it will be moving its “Checkpoint” as well. The new “Checkpoint” is conveniently placed around its “Ramp."

The final step is to add basically a game over screen or a celebration VFX. For this I had to go into Assets > Karting > Prefabs > VFX > CheckpointConfetti. Select a “Checkpoint” in the Hierarchy that I want to modify. Each “Checkpoint” has a field in its Inspector called “Spawn Prefab On Pickup”.

Next, I Drag the "CheckpointConfetti” prefab into the Spawn Prefab on Pickup field in the Inspector window. Next, I set the Destroy Spawn Prefab to 5 seconds. When the player reaches the checkpoint, it will spawn the “CheckpointConfetti” prefab and then destroy it in 5 seconds.

I ran a quality check and played a test game on my final product prior to submission, to ensure all the components were in place and functioning as per intended design and specifications.

I conclude my ReadMe submission for my Final Project on CS50 Introduction to Game Design.  For questions/comments/suggestions please contact me at tmurikken@yahoo.com

 
