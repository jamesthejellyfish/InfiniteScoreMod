# InfiniteScoreMod
A mod for balatro that increases the maximum score from 1.7e308 to effectively infinite.

Requires [Steammodded](https://github.com/Steamopollys/Steamodded)

Go to [releases](https://github.com/jamesthejellyfish/InfiniteScoreMod/releases), download InfiniteScore.zip, unzip and place all files in C:/Users/your username/AppData/Roaming/Balatro/Mods/ (you may have to make this folder)

# Compatibility Warning
- This mod makes significant changes to base functions that exist in the game. Because of this, this mode will likely not be compatible with other mods without significant tweaking.
- InfiniteScore has been tested with Steamodded version 0.7.2. More recent versions may break this mod.

Thanks to thenumbernine for their [bignumber library](https://github.com/thenumbernine/lua-bignumber/), which I adapted as the basis for this mod.

# features
- allows for the blind amount and chips scored to exceed the game's current maximum of the 64 bit double maximum value (~1.7e308)
![Scoring hand](Screenshots/scoring.png)

- The ante continues to scale exponentially, and can theoretically continue on forever.
![500 ante](Screenshots/ante%20500.png)

- also includes a challenge that starts at ante 39 and a build that can score past the previous score cap, as an illustration of the mod's functionality.
# Known Issues
- As can be seen in the previous screenshot, the visual scaling for both the ante and the mult and chips is pretty broken as I did not have a perfect understanding of how it worked so just left it as-is.
- it is quite possible that things will break if you exit out of a game and try to enter again, as the change in datatype required a major rehaul of the saving and loading functions for blind information.
- The bignumber library is very unstable and prone to breaking, especially with larger numbers (>e5000). There are likely a myriad of bugs that I have not caught in testing. Feel free to post an issue describing the bug and I will hopefully address it in a subsequent release.
