# Clickable Cube Transition


A 3D Cube transition for your PageView and PageRoute.

This is a fork of [this plugin](https://github.com/aeyrium/cube_transition) that demonstrate how to make items of PageView Cube Transition clickable.

The issue was that a Stack() is used in CubeWidget class. This is needed for the final effect: it adds a black layer on top of items and its opacity decreases gradually based on de scroll position. The problem is that every face of the cube has this layer on top of it (with opacity = 0 when not scrolling) so the accual widget below it is not. 

The solution was simply to check if the user is currently scrolling or not and, if a scroll is in progress render the accual Stack with the effect, othersie render only the accual widget. 

<p align="center">
  <img src="https://media.giphy.com/media/gsnmnzFDRzGZZwJxGa/giphy.gif">
</p>
