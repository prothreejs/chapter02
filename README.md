# Capitulo 2

## Descripcion 🚀

_Este capitulo contiene la modificacion de los archivos index.html, script.js y style.css agregando codigo para la primera practica implementando las definiciones de Three.js._

### Modificar el archivo index.html agregando las siguientes lineas de codigo. 📋

```
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>Hola Mundo con three.js</title>
		<link rel="stylesheet" href="/style.css" type="text/css" >
	</head>
<body>
	<script type="module" src="/script.js"></script>
</body>
</html>
```
### Modificar el archivo script.js agregando las siguientes lineas de codigo. 📋

```
import * as THREE from 'three';

const scene = new THREE.Scene();

const camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

const renderer = new THREE.WebGLRenderer();
renderer.setSize( window.innerWidth, window.innerHeight );

document.body.appendChild( renderer.domElement );

const geometry = new THREE.BoxGeometry( 1, 1, 1 );

const material = new THREE.MeshBasicMaterial( { color: 0x00ff00 } );

const cube = new THREE.Mesh( geometry, material );

scene.add( cube );
camera.position.z = 5;

function animate() { 
	requestAnimationFrame( animate );
	cube.rotation.x += 0.01;
	cube.rotation.y += 0.01;
	renderer.render( scene, camera );
}
animate();
```
### Modificar el archivo style.css agregando las siguientes lineas de codigo. 📋

```
body { margin: 0; }
```
### Compilar y desplegar 📋

_Descarga o clona el proyecto tu maquina local y compila con **NPM** sobre la ruta del la carpeta chapter02 ejecutar lo siguientes 2 comandos_

```
]$ npm install
```
```
]$ npm run dev
```
**Copia y pega en un navegador web la URL resultante http://localhost:5173/ y ve el resultado** 

## Construido con 🛠️

_El proyecto esta contruido con las siguientes herramientas:_

* [Three.js](https://threejs.org/) - Lenjuage de programacion JavaScript.
* [Node.js-NPM](https://nodejs.org/en) - Manejador de paquetes.
* [VisualStudio](https://visualstudio.microsoft.com/es/) - El framework usado para compilar y ejecutar el codigo JavaScript.
## Autores ✒️

_Autores del proyecto:_

* **Carlos Nieblas** - *Idea original*
* **Omar Santiago** - *Me subi al avion, total que puede pasar!*

## Licencia 📄

Este proyecto está bajo la Licencia (Invitme un cafe).

## Contacto 📄

* **email** - [prothreejs@gmail.com](https://mail.google.com/)
* **github** - [prothreejs](https://github.com/prothreejs)
* **instagram** - [progamestreejs](https://www.instagram.com/)
* **facebook** - [progamestreejs](https://www.facebook.com/profile.php?id=61558214141911)

---
⌨️ con ❤️ por [cnieblas](https://www.cnieblas.com) y osantiago.
