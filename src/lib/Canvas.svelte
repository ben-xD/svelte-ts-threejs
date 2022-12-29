<script lang="ts">
    import * as THREE from 'three';
    import {onMount} from "svelte";

    const scale = 3
    const width = 160 * scale;
    const height = 90 * scale;

    let canvas;
    onMount(() => {
        canvas.height = height;
        canvas.width = width;
        const scene = new THREE.Scene();

        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        const camera = new THREE.PerspectiveCamera(75, width / height, 0.1, 1000);

        const renderer = new THREE.WebGLRenderer({canvas});
        renderer.setSize(width, height);

        const geometry = new THREE.BoxGeometry(10, 10, 10);
        const material = new THREE.MeshBasicMaterial({color: '#00ff00'});
        const cube = new THREE.Mesh(geometry, material);
        scene.add(cube);

        camera.position.z = 25;

        function animate() {
            requestAnimationFrame(animate);
            cube.rotation.x += 0.01;
            cube.rotation.y += 0.01;
            renderer.render(scene, camera);
        }

        animate();
    })
</script>

<canvas bind:this={canvas}></canvas>
