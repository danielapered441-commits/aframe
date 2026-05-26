<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Experiencia VR - Tenis</title>
  <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
</head>
<body>
<a-scene background="color: #87CEEB">

  <!-- Suelo tipo parque -->
  <a-plane position="0 0 0" rotation="-90 0 0" width="30" height="30"
           color="#4CAF50" shadow></a-plane>

  <!-- Árboles decorativos -->
  <a-cylinder position="-4 1 -5" radius="0.2" height="2" color="#8B4513"></a-cylinder>
  <a-sphere position="-4 2.5 -5" radius="1.2" color="#228B22"></a-sphere>

  <a-cylinder position="4 1 -6" radius="0.2" height="2" color="#8B4513"></a-cylinder>
  <a-sphere position="4 2.5 -6" radius="1.2" color="#228B22"></a-sphere>

  <!-- TENIS 3D - reemplaza la URL con tu archivo subido a Glitch -->
  <a-entity
    gltf-model="url(TU_ARCHIVO.glb)"
    position="0 1 -3"
    scale="2 2 2"
    animation="property: rotation; to: 0 360 0; loop: true; dur: 6000">
  </a-entity>

  <!-- Panel con texto de la marca -->
  <a-plane position="0 2.5 -4" width="3" height="1" color="#000000" opacity="0.7">
  </a-plane>
  <a-text value="NOMBRE DE LA MARCA\nEl tenis que te lleva más lejos"
          position="-1.3 2.5 -3.9"
          color="white" width="3.5"></a-text>

  <!-- Cámara con controles para mover la vista -->
  <a-camera>
    <a-cursor color="white"></a-cursor>
  </a-camera>

  <!-- Luz -->
  <a-light type="ambient" intensity="0.8"></a-light>
  <a-light type="directional" position="2 4 3" intensity="1"></a-light>

</a-scene>
</body>
</html>
