## Better EdPuzzle Userscript

Speed up, allow skipping, and stop auto-pausing on EdPuzzle.com.

## Installation

Install a userscript manager like Tampermonkey or Greasymonkey on your web browser. (This script was built with Tampermonkey on Firefox, but it should work everywhere.)

Once you have a userscript manager installed you can use this convenient install link:
[Install](https://github.com/Enchoseon/better-edpuzzle-userscript/raw/main/better-edpuzzle-userscript.user.js)

## Current Functionality

EdPuzzle has a wide variety of media sources, each with varying protections, most of which are yet to be broken.

Please note that these media source values were pulled from EdPuzzle's minified code (with the exception of *youtube-nocookies.com*)—and since there's no documentation, I have no idea what they mean, I sort of just have to open random EdPuzzles and look at the API response myself & work backwards from there.

**Media Source**        | **Speedhack** | **Anti Auto-Pause** | **Force Allow Skipping** |
------------------------|---------------|---------------------|--------------------------|
YOUTUBE                 | Yes           | Yes                 | Yes                      |
VIMEO                   | No            | Yes                 | Yes                      |
VIMEO_WITH_CONTROLS     | No            | Yes                 | Yes                      |
EDPUZZLE                | No            | Yes                 | Yes                      |
FILE                    | No            | Yes                 | Yes                      |
youtube-nocookies.com   | No            | Yes                 | Yes                      |

**Important Note for Learning Management Systems**: The media source value is an internal API value, some videos marked "EdPuzzle" may use a special YouTube player that uses *youtube-nocookies.com*. I've seen this happen with private videos that need a one-time token from a learning management system like Canvas, Schoology, Moodle, Blackboard, PowerSchool, & Blackbaud.

## To-Do

- Get speedhack to work on more media source types.
  - If anyone understands setters & getters, please read [this gist](https://gist.github.com/SheepTester/a5009c402d58117b167049faa274de52)—I think it's the key to getting the speedhack to work on EdPuzzle media source videos.
- Add a new right-click context menu option to open the video source in another tab.
