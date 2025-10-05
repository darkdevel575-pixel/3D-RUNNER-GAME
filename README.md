<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>3D Runner Game - Deluxe</title>
  <style>
    body { margin: 0; overflow: hidden; background: #000; }
    canvas { display: block; }
    #score {
      position: absolute;
      top: 10px;
      left: 10px;
      color: white;
      font-size: 22px;
      font-family: Arial, sans-serif;
    }
  </style>
</head>
<body>
  <div id="score">Score: 0</div>
  <script src="https://cdn.jsdelivr.net/npm/three@0.156.1/build/three.min.js"></script>
  <script>
    const scene = new THREE.Scene();
    scene.fog = new THREE.Fog(0x000000, 5, 60);

    // Camera
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    const renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.body.appendChild(renderer.domElement);

    // Lighting# 3D-RUNNER-GAME
