# UnrealTestMap-2022

During my Game Design studies, I had to create a test map for the basic character controller in Unreal Engine.

![testmap-topview](https://user-images.githubusercontent.com/96313983/187083381-1c6cd507-6844-4be0-b5bd-496ca7fe76c8.jpg)


### Organizing tests

I chose to divide the map in 4 sections with a theme on each one:
- Elevation : shapes to test collisions between the character and the floor
- Jump : platforms spaced with different heights and distances to test jumps
- Interiors : walls and ceilings to test character and camera collisions
- Objects : a set of objets with various shapes and sizes to test physics

On start, the player is located on the center of the map to avoid spending time running from a section to another.

![testmap-sections](https://user-images.githubusercontent.com/96313983/187083390-d31da9e1-8566-40cf-8238-79bc8e854f38.jpg)

---

<img width="400" src="https://user-images.githubusercontent.com/96313983/187083400-81e46c15-1ad2-4508-91be-e7e6db0647ad.jpg">

> The window is located at 0,50m from the ground with a 2m gap height

<br>

<img width="400" src="https://user-images.githubusercontent.com/96313983/187083407-8db7f33e-f953-49fc-bd62-ccee741ba0e2.jpg">

> It's impossible to jump at a 2,50m height



All the elements in the map have indications (size, height, distance, gap) in case the developers need to know what specific conditions triggers a bug. I tried to put them at strategic places to be understood by anyone discovering the map for the first time.
I also added green and red materials on specific elements to indicate that an action is or isn't possible. Then, if the character controller changes in the future, this materials can help as non-regression tests.


### Final result

![testmap-example (1)](https://user-images.githubusercontent.com/96313983/187084969-0006c87e-dca8-4ef1-9606-f94b528c708b.gif)


Here is a <a href="https://drive.google.com/file/d/1NAiCJVAwfxyqh0MYRtRiHL9NGKFPWLTt/view" target="_blank">video of the test map</a> where I explain every sections elements.

The purpose of the exercice only was to make the map, not to fix bugs on the character controller. That's why there are bugs and the map illustrates how easy the developers could find them.




