# Clickable Cube Transition


A 3D Cube transition for your PageView and PageRoute.

This is a fork of [this plugin](https://github.com/aeyrium/cube_transition) that demonstrate how to make items of PageView Cube Transition clickable.

The issue was that a Stack() is used in CubeWidget class. This is needed for the final effect: it adds a black layer on top of items and its opacity decreases gradually based on the scroll position. The problem is that every face of the cube has this layer on top of it (with opacity = 0 when not scrolling) so the accual widget below is not clickable. 

The solution was simply to check if the user is currently scrolling or not and if a scroll is in progress render the actual Stack with the effect, otherwise render only the accual widget. 


  ![cube demo](https://user-images.githubusercontent.com/38936570/177825545-c688681f-ab7a-4307-a4c8-891f3ebc0177.gif)


