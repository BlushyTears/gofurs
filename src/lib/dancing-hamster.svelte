<script>
  import HamsterGIF from "../assets/hamster-dance.gif";

  let top = "50%";
  let left = "50%";

  function moveGif() {
    // Calculate new random position within the viewport
    // Adjust the max values based on your viewport and gif size for better positioning
    const newTop = Math.random() * (window.innerHeight - 100); // Subtract GIF height for better positioning
    const newLeft = Math.random() * (window.innerWidth - 100); // Subtract GIF width for better positioning

    // Update top and left values
    top = `${newTop}px`;
    left = `${newLeft}px`;
  }

  function handleKeydown(event) {
    // Check if the key is Enter or Space
    if (event.key === "Enter" || event.key === " ") {
      moveGif();
      event.preventDefault(); // Prevent the default action for these keys
    }
  }
</script>

<div
  class="gif-container"
  on:mouseover={moveGif}
  on:focus={moveGif}
  on:keydown={handleKeydown}
  tabindex="0"
  role="button"
  aria-label="Move GIF to a new location"
  style="top: {top}; left: {left};"
>
  <img src={HamsterGIF} alt="Hover to move GIF" />
</div>

<style>
  .gif-container {
    position: fixed;
    transition:
      top 0.5s ease,
      left 0.5s ease; /* Smooth transition for moving effect */
    cursor: pointer; /* Change cursor to indicate interactiveness */
    z-index: 999;
  }
  .gif-container img {
  width: 200px; /* Set your desired width */
  height: 200px; /* Set your desired height */
}
</style>
