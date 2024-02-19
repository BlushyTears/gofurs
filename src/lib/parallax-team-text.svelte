<script>
  import { onMount } from "svelte";
  export let text = ""; // Text to display
  let posY = 0;
  let offset = 0;

  function updateScroll() {
    posY = window.scrollY;
    offset = posY * 0.2; // Adjust this value to change the effect intensity
  }

  onMount(() => {
    window.addEventListener("scroll", updateScroll);
    return () => {
      window.removeEventListener("scroll", updateScroll);
    };
  });
</script>

<h1 style="transform: translateY({offset}px);">
  {text}
</h1>

<style>
  
  h1 {
    margin: 0 auto;
    z-index: 2;
    text-align: center;
    color: rgba(0,0,0, 0.8);
    font-family: "Arial", sans-serif;
    font-size: calc(3em + 2vw);
    font-weight: bold;
    margin-bottom: 2rem;
    border-radius: 1px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
    width: calc(30% + 10rem);
    padding: 3rem;
  }
</style>
