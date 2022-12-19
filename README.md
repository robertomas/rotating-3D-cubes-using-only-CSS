# rotating-3D-cubes-using-only-CSS
This code creates three rotating 3D cubes using ONLY CSS.


This code creates three rotating 3D cubes using CSS.

The style element contains the styles for the cubes and their faces. The .flex class is used to create a flex container for the three cubes. The .scene class sets the width, height, border, and margin of each cube, and also sets the perspective from which the 3D cubes will be viewed.

The .cube class sets the width, height, position, transform style, and initial transform for each cube. It also includes a transition effect and an animation to rotate the cube around the y-axis. The .cube.second and .cube.all classes override the default animation with animations to rotate the cube around the x-axis and both the x and y axes, respectively.

The .cube-face class sets the position, size, border, font, and color for each face of the cube. The .face-front, .face-back, .face-right, .face-left, .face-top, and .face-bottom classes set the background color and transform for each face of the cube.

The @keyframes rules define the animations for the cubes. The rotate, rotateX, and rotateAll animations specify the starting and ending transforms for the cubes, creating the rotation effect.
