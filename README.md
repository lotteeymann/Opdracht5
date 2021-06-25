# Opdracht5
Interaction

![wood](https://user-images.githubusercontent.com/86419683/123458679-9a6d1800-d5e5-11eb-9a73-477f0a91fbe1.jpg)
![wood2](https://user-images.githubusercontent.com/86419683/123458690-9e009f00-d5e5-11eb-9601-db647175fb68.jpg)
![grass](https://user-images.githubusercontent.com/86419683/123458704-a1942600-d5e5-11eb-8ec8-d1a127d1e0f2.jpg)

![media.js](https://github.com/lotteeymann/Opdracht5/blob/e96ef62b797362906172e67c0918dd550d883b42/main.js)

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Hello, WebVR! • A-Frame</title>
    <meta name="viewport" content="width=device-width">
    <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
    <script src="scripts/main.js" defer></script>
  </head>
  <body>
    <a-scene background="color: #333333">
      <a-assets>
          <img id="wood" src="wood.jpg" />
          <img id="wood2" src="wood2.jpg" />
          <img id="grass" src="grass.jpg" />
      </a-assets>

      <a-entity id="mouseCursor" cursor="rayOrigin: mouse"></a-entity>

      <a-box id="myBox" 
        position="-1 1 -3" 
        rotation="0 45 0" 
        width="3" 
        height="1" 
        depth="1" 
        material="src: #wood"
        shadow 
        animation__mouseenter="
          property: components.material.material.color; 
          type: color; 
          to: blue; 
          startEvents: mouseenter; 
          dur: 500;"
        animation__mouseleave="
          property: components.material.material.color; 
          type: color; 
          to: red; 
          startEvents: mouseleave; 
          dur: 500;">  
      </a-box>
      <a-box id="myOtherBox" 
        position="2 1 -3" 
        rotation="0 45 0" 
        width="3" 
        height="1" 
        depth="1" 
        material="src: #wood"
        shadow>  
      </a-box>
      <a-plane id="ground"
        position="0 0 -4" 
        rotation="-90 0 0" 
        width="100" 
        height="100" 
        color="#7BC8A4" 
        material="src: #grass; repeat: 10 10"
        shadow>
      </a-plane> 
    </a-scene>
  </body>
</html>
