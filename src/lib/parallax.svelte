<script>
  import { onMount } from "svelte";
  export let teamMember;

  let posY = 0;

  onMount(() => {
    window.addEventListener("scroll", () => {
      posY = window.pageYOffset;
    });

    return () => {
      window.removeEventListener("scroll", () => {
        posY = window.pageYOffset;
      });
    };
  });
</script>

<div
  class="outer-parallax"
  style="transform: translate3d(0px, {posY * 0.17}px, 0px);"
>
  <div class="flip-container">
    <div class="parallax">
      <div
        class="front"
        style="background-image: url('{teamMember.image}');"
      ></div>
      <div class="back">
        <br />
        <h2 style="text-align: center;">{teamMember.title}</h2>
        <br />

        <p style="text-align: center;">{teamMember.description}</p>
      </div>
    </div>
  </div>
</div>

<style>
  h2 {
    font-size: calc(0.6em + 1.2vw);
  }

  p {
    font-size: calc(0.5em + 0.15vw);
  }

  p,
  h2 {
    width: 97%;
    margin: 0 auto;
  }

  @keyframes rotateBorderGradient {
  0%, 100% {
    border-image: linear-gradient(45deg, #5628b4, #dd33fa, #ff4d4d) 1; /* More saturated colors */
  }
  50% {
    border-image: linear-gradient(135deg, #5628b4, #dd33fa, #ff4d4d) 1; /* More saturated colors */
  }
}

  .outer-parallax {
    border-radius: 0.2rem;
    perspective: 100px;
    width: 50%;
    min-width: 20rem;
    max-width: 45rem;
    height: calc(20rem + 5vw);
    max-height: calc(20rem + 5vw);
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;

    border: 3px solid transparent;
    border-image-slice: 1;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
    animation: rotateBorderGradient 2s infinite;

    border-image-repeat: stretch;
  }

  .flip-container {
    width: 100%;
    height: 100%;
    position: relative;
  }

  .parallax {
    width: 100%;
    height: 100%;
    transition: transform 0.7s;
    transform-style: preserve-3d;
  }

  .flip-container:hover .parallax {
    transform: rotateY(180deg);
  }

  .front,
  .back {
    backface-visibility: hidden;
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    font-size: 20px;
  }

  .front {
    background-size: cover;
  }

  .back {
    color: white;
    background-image: linear-gradient(135deg, #d35400 0%, #8e44ad 100%);
    transform: rotateY(180deg);
    font-size: 1.5em;
    display: block;
  }
</style>
