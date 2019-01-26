# [Weekly Report]({% post_url 2019-01-18-weekly-report %})

## Things I Did
- Setup Transparent aero overlay from [https://github.com/ReactiioN1337/aero-overlay](https://github.com/ReactiioN1337/aero-overlay)
- Added lag fix for windows 10 RS2 from one of the fork's commit [https://github.com/rossnichols/aero-overlay/commit/969397f0fe47fc0caddef294e6ef398e13cc1c67](https://github.com/rossnichols/aero-overlay/commit/969397f0fe47fc0caddef294e6ef398e13cc1c67)
- Calling scale_overlay function inside a loop to follow target window everytime the user moves it.
- Studied the imgui documentation and modified the overlay to implement directx9 implementation of imgui.
- Used directx9 example from [https://github.com/ocornut/imgui/tree/master/examples](https://github.com/ocornut/imgui/tree/master/examples) to integrate imgui with the aero overlay.
- Integrated imgui input system with the aero overlay's window_procedure hook.
- Integrated imgui renderer with aero overlay's Direct3D9 Device.
- Added imgui demo GUI for testing the integration.

## Things I Am Going To Do
- Removing the demo functionality.
- Creating a dummy GUI for one of my game hacking projects.
- Documenting usage and creating a powerpoint presentation.

## Deliverables
- Source for the overlay with imgui implemented and a dummy GUI.
- A compiled exe which will recieve name of any open window as an argument. It will create an overlay on the specified window and a dummy GUI will be drawn on that overlay.
- Usage Intructions

## Problems
- Scaling the target window also scales the stuff being rendered on the overlay.

## Workarounds
- The aero overlay comes with Direct2D and Direct3D renderers but i only found out directx9 implementation of imgui. So the gui is only drawn when the device argument is set to "d3d9".
- The aero overlay is click through so the imgui windows does not receive any mouse or keyboard input. So in order to fix it i am using a solution provided here [https://www.unknowncheats.me/forum/1474150-post9.html](https://www.unknowncheats.me/forum/1474150-post9.html). What it basically does is the user can toggle the gui and while it is rendering the overlay's click thorugh behaviour is disabled and when the gui is not rendering the click through behaviour of overlay is enabled.

## Screenshots
- Drawing demo imgui over windows 10 calculator
![imgui demo](https://tejisav.github.io/Demo.jpg "ImGui Demo")
