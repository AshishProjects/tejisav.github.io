# [Final Report]({% post_url 2019-01-25-final-report %})

## Things I Did This Week
- Removed the demo functionality.
- Played with all the available customisation options, widgets, controls and layouts.
- Created a layout based on one of my previous hacks for PUBG
- Styled the layout

## Evaluation
- I was mostly able to complete my task in time, although i found out there were some complications with the input system on transparent click through overlays but i found a workround for it that i posted in the previous weekly report

## Lessons Learned
- In depth knowledge about Dear ImGui like implementation, styling, controls
- Was able to create a much better base for game hacking than the previous one's
- Overall programming knowledge in C++

## Unexpected Challenges
- The aero overlay comes with Direct2D and Direct3D renderers but i only found out directx9 implementation of imgui. So the gui is only drawn when the device argument is set to "d3d9".
- The aero overlay is click through so the imgui windows does not receive any mouse or keyboard input. So in order to fix it i am using a solution provided here [https://www.unknowncheats.me/forum/1474150-post9.html](https://www.unknowncheats.me/forum/1474150-post9.html). What it basically does is the user can toggle the gui and while it is rendering the overlay's click thorugh behaviour is disabled and when the gui is not rendering the click through behaviour of overlay is enabled.
- Scaling the target window also scales the stuff being rendered on the overlay.

## Future Work
- I will be porting all the stuff from my old base to this new base I created.
- It will also help me in my future game hacking projects
- Overlays with GUI are not only limited to game hacking, they can also be used in gaming clients, team speak software's e.g. Discord, Steam both have their overlays with GUI’s that provide functionality for their application directly in the game.

## Screenshots
- Drawing demo imgui over windows 10 calculator
![imgui demo](https://tejisav.github.io/Demo.jpg "ImGui Demo")
