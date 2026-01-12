[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# MG1
## Devlog
Yan Zhang

Since I didn’t attend the Week 1 activity, I started MG1 by making my own simple plan based on the assignment. I broke the project into a few parts: getting the player to move, figuring out how planting should work, updating the UI, and setting up the prefab for the plant. From the beginning, I knew the Player script would handle all the gameplay, and the UI would be handled separately in the PlantCountUI script.


In the Player class, I set up fields for speed, seed counts, the player’s Transform, the prefab, and a reference to PlantCountUI. My idea was that Update() would constantly check for movement input and then detect when the player pressed the space bar. That ended up working exactly as I expected—using Input.GetAxisRaw() for movement and calling PlantSeed() when space was pressed.

For the UI, I tried to keep it separate from the gameplay code. The Player script just sends numbers to UpdateSeeds(int seedsLeft, int seedsPlanted) in PlantCountUI, which updates the TMP_Text. This made it easier to keep things organized without cluttering the Player script.


One thing I changed while coding was how I handled the initial UI setup. At first, I wanted to set the UI values directly inside the Player script, but after looking at the example structure, it made more sense to let PlantCountUI handle all the UI text updates. It kept everything cleaner and made the code easier to read.


If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites
