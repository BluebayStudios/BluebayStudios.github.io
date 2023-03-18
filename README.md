<!DOCTYPE html>
<html>
<head>
	<title>Bluebay's Unblocked Games</title>
	<style>
		body {
			background-color: #111;
			margin: 0;
			padding: 0;
			overflow: hidden;
		}
		canvas {
			display: block;
			position: fixed;
			top: 0;
			left: 0;
			z-index: -1;
		}
		h1 {
			color: #fff;
			text-align: center;
			font-family: 'Helvetica Neue', sans-serif;
			font-weight: bold;
			font-size: 5em;
			margin-top: 50px;
			text-shadow: 0px 0px 10px rgba(255, 255, 255, 1);
			-webkit-animation: glow 1s ease-in-out infinite alternate;
			-moz-animation: glow 1s ease-in-out infinite alternate;
			animation: glow 1s ease-in-out infinite alternate;
		}
		@-webkit-keyframes glow {
			from {
				text-shadow: 0px 0px 10px rgba(255, 255, 255, 1);
			}
			to {
				text-shadow: 0px 0px 20px rgba(255, 255, 255, 0.5);
			}
		}
		@-moz-keyframes glow {
			from {
				text-shadow: 0px 0px 10px rgba(255, 255, 255, 1);
			}
			to {
				text-shadow: 0px 0px 20px rgba(255, 255, 255, 0.5);
			}
		}
		@keyframes glow {
			from {
				text-shadow: 0px 0px 10px rgba(255, 255, 255, 1);
			}
			to {
				text-shadow: 0px 0px 20px rgba(255, 255, 255, 0.5);
			}
		}
	</style>
</head>
<body>
	<h1>Glowing Particles</h1>
	<canvas id="canvas"></canvas>
	<script>
		var canvas = document.getElementById('canvas');
		var ctx = canvas.getContext('2d');
		var particles = [];
		var particleCount = 50;
		var particleRadius = 2;
		var speed = 2;
		
		// Set canvas size
		canvas.width = window.innerWidth;
		canvas.height = window.innerHeight;
		
		// Particle constructor function
		function Particle(x, y) {
			this.x = x;
			this.y = y;
			this.vx = (Math.random() - 0.5) * speed;
			this.vy = (Math.random() - 0.5) * speed;
			this.radius = particleRadius;
		}
		
		// Add particles to array
		for (var i = 0; i < particleCount; i++) {
			var x = Math.random() * canvas.width;
			var y = Math.random() * canvas.height;
			particles.push(new Particle(x, y));
		}
		
		// Animation loop
		function animate() {
			requestAnimationFrame(animate);
			
			// Clear canvas
			ctx.clearRect(0, 0, canvas.width, canvas.height);
			
			// Draw particles
			ctx.fillStyle = '#fff';
			for (var i = 0; i < particles.length;
