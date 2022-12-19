# rotating-3D-cubes-using-only-CSS
This code creates three rotating 3D cubes using ONLY CSS.


This code creates three rotating 3D cubes using CSS.

The style element contains the styles for the cubes and their faces. The .flex class is used to create a flex container for the three cubes. The .scene class sets the width, height, border, and margin of each cube, and also sets the perspective from which the 3D cubes will be viewed.

The .cube class sets the width, height, position, transform style, and initial transform for each cube. It also includes a transition effect and an animation to rotate the cube around the y-axis. The .cube.second and .cube.all classes override the default animation with animations to rotate the cube around the x-axis and both the x and y axes, respectively.

The .cube-face class sets the position, size, border, font, and color for each face of the cube. The .face-front, .face-back, .face-right, .face-left, .face-top, and .face-bottom classes set the background color and transform for each face of the cube.

The @keyframes rules define the animations for the cubes. The rotate, rotateX, and rotateAll animations specify the starting and ending transforms for the cubes, creating the rotation effect.


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Rotating 3D cubes using ONLY CSS</title>
    <style>
        /* Flex container for the 3D cubes */
        .flex {
            display: flex;
        }

        /* Style for the container of each 3D cube */
        .scene {
            width: 200px;
            height: 200px;
            border: 1px solid #ccc;
            margin: 80px;
            perspective: 400px;
        }

        /* Style for each 3D cube */
        .cube {
            width: 200px;
            height: 200px;
            position: relative;
            transform-style: preserve-3d;
            transform: translateZ(-100px);
            transition: transform 1s;
            /* Rotate the cube around the y-axis */
            animation: rotate 3s ease-in-out infinite;
        }

        /* Rotate the cube around the x-axis */
        .cube.second {
            animation: rotateX 3s ease-in-out infinite;
        }

        /* Rotate the cube around both the x and y axes */
        .cube.all {
            animation: rotateAll 3s ease-in-out infinite;
        }

        /* Style for each face of the 3D cube */
        .cube-face {
            display: flex;
            justify-content: center;
            align-items: center;
            position: absolute;
            width: 200px;
            height: 200px;
            border: 2px solid #000;
            font-size: 40px;
            font-weight: bold;
            color: #ccc;
            text-align: center;
        }

        /* Style for the front face of the 3D cube */
        .face-front {
            background: hsla(0, 100%, 50%, 0.7);
            /* Position the front face in the front of the 3D cube */
            transform: rotateY(0deg) translateZ(100px);
        }

        .face-back {
            background: hsla(60, 100%, 50%, 0.7);
            transform: rotateY(90deg) translateZ(100px);
        }

        .face-right {
            background: hsla(120, 100%, 50%, 0.7);
            transform: rotateY(180deg) translateZ(100px);
        }

        .face-left {
            background: hsla(180, 100%, 50%, 0.7);
            transform: rotateY(-90deg) translateZ(100px);
        }

        .face-top {
            background: hsla(240, 100%, 50%, 0.7);
            transform: rotateX(90deg) translateZ(100px);
        }

        .face-bottom {
            background: hsla(300, 100%, 50%, 0.7);
            transform: rotateX(-90deg) translateZ(100px);
        }

        /* Animation to rotate the 3D cube around the y-axis */
        @keyframes rotate {
            from {
                transform: rotateY(0deg);
            }
            to {
                transform: rotateY(360deg);
            }
        }

        /* Animation to rotate the 3D cube around the x-axis */
        @keyframes rotateX {
            from {
                transform: rotateX(0deg);
            }
            to {
                transform: rotateX(360deg);
            }
        }

        /* Animation to rotate the 3D cube around both the x and y axes */
        @keyframes rotateAll {
            from {
                transform: rotateY(0deg) rotateX(0deg);
            }
            to {
                transform: rotateY(360deg) rotateX(360deg);
            }
        }
    </style>
</head>
<body>
<!-- Flex container for the 3D cubes -->
<div class="flex">
    <!-- Container for the first 3D cube -->
    <div class="scene">
        <!-- First 3D cube -->
        <div class="cube">
            <!-- Front face of the first 3D cube -->
            <div class="cube-face face-front">front</div>
            <!-- Back face of the first 3D cube -->
            <div class="cube-face face-back">back</div>
            <!-- Right face of the first 3D cube -->
            <div class="cube-face face-right">right</div>
            <!-- Left face of the first 3D cube -->
            <div class="cube-face face-left">left</div>
            <!-- Top face of the first 3D cube -->
            <div class="cube-face face-top">top</div>
            <!-- Bottom face of the first 3D cube -->
            <div class="cube-face face-bottom">bottom</div>
        </div>
    </div>

    <div class="scene">
        <div class="cube second">
            <div class="cube-face face-front">front</div>
            <div class="cube-face face-back">back</div>
            <div class="cube-face face-right">right</div>
            <div class="cube-face face-left">left</div>
            <div class="cube-face face-top">top</div>
            <div class="cube-face face-bottom">bottom</div>
        </div>
    </div>

    <div class="scene">
        <div class="cube all">
            <div class="cube-face face-front">front</div>
            <div class="cube-face face-back">back</div>
            <div class="cube-face face-right">right</div>
            <div class="cube-face face-left">left</div>
            <div class="cube-face face-top">top</div>
            <div class="cube-face face-bottom">bottom</div>
        </div>
    </div>
</div>

</body>
</html>

```
