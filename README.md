# Three JS 

## Basics

### Renderer, Scene & Camera

Here are the minimum components:
1) Scene setup
2) Camera setup
3) Renderer setup

<img src="img/threejs-structure.svg" width="400px">

```
var renderer = new THREE.WebGLRenderer({antialias: true});

var scene = new THREE.Scene();

var camera = new THREE.PerspectiveCamera(75,window.innerWidth/window.innerHeight,0.1,1000);

document.body.appendChild(renderer.domElement);

camera.updateProjectionMatrix();

// You pass a Scene and a Camera to a Renderer and it renders (draws) the portion of the 3D scene.
var render = function() {
            requestAnimationFrame(render);        
            renderer.render(scene, camera);
         }
render();
```

### Mesh

Class representing triangular polygon mesh based objects.

**Mesh( geometry : BufferGeometry, material : Material )**
* geometry — (optional) an instance of BufferGeometry. Default is a new BufferGeometry.
* material — (optional) a single or an array of Material. Default is a new MeshBasicMaterial

## Resources
- [][ThreeJS Fundamentals](https://threejs.org/manual/#en/fundamentals)