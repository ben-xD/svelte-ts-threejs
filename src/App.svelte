<script lang="ts">
  import svelteLogo from './assets/svelte.svg'
  import threejsLogo from './assets/threejs.png'
  import Canvas from './lib/Canvas.svelte'
</script>

<main>
  <div>
    <a href="https://vitejs.dev" target="_blank" rel="noreferrer"> 
      <img src="/vite.svg" class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer"> 
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
    <a href="https://threejs.org/" target="_blank" rel="noreferrer">
      <img src={threejsLogo} class="logo threejs" alt="Three.js Logo" />
    </a>
  </div>
  <h1>Vite + Svelte + Three.js</h1>

  <div class="card">
    <Canvas />
  </div>

  <p class="read-the-docs">
    Click on the logos to learn more
  </p>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>