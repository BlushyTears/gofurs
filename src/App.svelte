<script>
  import Wallpaper from "./assets/frens.png";
  import ParallaxText from "./lib/parallax-team-text.svelte";
  import DancingHamster from "./lib/dancing-hamster.svelte";

  // Team section stuff
  import Parallax from "./lib/parallax.svelte";
  import camo from "./assets/camo.webp";
  import gizmo from "./assets/gizmo.webp";
  import minty from "./assets/minty.webp";
  import neon from "./assets/neon.webp";
  import rusty from "./assets/rusty.webp";
  import skyler from "./assets/skyler.webp";

  // Buy Component
  import PulseBuy from "./lib/pulsebuy.svelte";
  import EthBuy from "./lib/ethbuy.svelte";
  import Pulsebuy from "./lib/pulsebuy.svelte";
  import Ethbuy from "./lib/ethbuy.svelte";
  
  // Only thing we use saos for is garnishing the user screen position and boolean state, so we can display the animation in a timely manner only once
  import Saos from "saos";

</script>

<!-- Adjusted container -->
<div class="wallpaper-clip-container">
  <img src={Wallpaper} alt="alternate text" class="wallpaper-image" />
</div>

<br />
<br />

<div class="section-1 red-theme">
  <h1 style="font-size: calc(1.4em + 2.2vw); width: 100%;">Good Old Fashioned Un Registered Security $GOFURS</h1>
  <br />
  <p style="font-size: calc(0.4em + 0.8vw); color: white;">
    BY PARTICIPATING YOU AGREE THAT YOU FULLY EXPECT 10 GAZILLION PERCENT
    PROFITS SOLELY FROM THE WORK OF THESE GOFURS
  </p>
  <br />
  <br />
  <br />
  <br />
  <!-- inline css since we want to highlight CA -->
  <p style="font-size: calc(0.5em + 1.5vw); color: white;">
    Contract: 0x54f667dB585b7B10347429C72c36c8B59aB441cb
  </p>
</div>

<div class="section-1 yellow-theme">
<Saos once={true}>
  <h1 class="left-slide">What is ERC-404</h1>
</Saos>
</div>

<br />
<br />

<div class="section-1 no-theme">
  <p style="font-size: 2em; color: #332809;">
    ERC404 is a new, experimental smart contract token standard. It has elements
    of normal ERC20 tokens and ERC721 NFTs...
  </p>
  <br />
</div>

<br />

<main>
  <ParallaxText text="Meet The Team" />
</main>

<br />
<br />
<br />
<br />
<br />
<br />
<br />

<main>
  <div class="team-members-container">
    <Parallax
      teamMember={{
        image: neon,
        title: 'Neon "Flash Drive" Glowpaw - Chief Executive Officer',
        description: `\"These neon synthwave glasses aren't just a fashion statement; they're a declaration of our bold vision for the future. As CEO, I'm leading our company towards new horizons, illuminated by innovative ideas and electrifying performance. Our investors are joining us on a journey to redefine what's possible, powering a brighter, richer future for everyone involved.\"`,
      }}
    />
    <Parallax
      teamMember={{
        image: gizmo,
        title: `Rusty "Gizmo 'Mega Byte' Furnandez" - Chief Technical Officer`,
        description: `"My purple glasses symbolize our innovative spirit and creative solutions in technology. We're not just following the digital evolution; we're leading it. Our breakthrough innovations are set to disrupt the industry, offering investors a unique opportunity to be part of a future where technology defines success.”`,
      }}
    />
    <Parallax
      teamMember={{
        image: minty,
        title: `Minty "Big Bank" Burrower - Chief Financial Officer`,
        description: `"Our financial strategies, as vibrant and forward-looking as my green glasses, are designed to ensure sustainable growth and profitability. We're not just managing assets; we're cultivating a fertile ground for investments to flourish, promising a rich harvest for our stakeholders."`,
      }}
    />
    <Parallax
      teamMember={{
        image: camo,
        title: `Camo “Lockdown” McTunnel - Chief Security Officer`,
        description: `"In a world where unpredictability is the only certainty, my military camo and steadfast demeanor stand as a testament to our unyielding security measures. Just like my hat blends yet stands out, we navigate the market's terrain with stealth and precision, ensuring our investors' assets are guarded with the utmost vigilance. Investing with us means your wealth is as secure as a bunker, promising not just growth but a fortress safeguarding your future. I'm Camo 'Lockdown' McTunnel, and with our strategic defenses, your investment is about to go on the offensive, multiplying in value while under the safest watch.”`,
      }}
    />
    <Parallax
      teamMember={{
        image: rusty,
        title: `Rusty "The Engine" Digwell - Chief Operations Officer`,
        description: `"With the same passion and intensity as my red glasses, we're streamlining operations to heat up the market. Our dynamic approach to challenges ensures efficiency and effectiveness, driving the company towards unprecedented operational success and profitability for our investors.”`,
      }}
    />
    <Parallax
      teamMember={{
        image: skyler,
        title: `Skyler "Buzzword" Whiskerton - Chief Marketing Officer`,
        description: `"The clarity and vision behind my blue glasses reflect our marketing strategies' depth and reliability. We're building strong, lasting connections with our audience, turning our brand into a legacy. Investing in us means investing in a company that values growth, engagement, and the power of a trusted brand.”`,
      }}
    />
  </div>
</main>

<div
  style="margin-top: 65rem;"
  class="section-1 yellow-theme"
>
  <Saos once={true}>
    <h1 class="right-slide">How to Buy GOFURS</h1>
  </Saos>
</div>


<div class="buy-container">
  <div>
    <br />
    <Pulsebuy />
  </div>

  <h2 style="font-size: 3.5em; margin-top: 1rem;">or</h2>

  <div>
    <br />
    <EthBuy />
  </div>
</div>

<div
  class="section-1 yellow-theme"
>
  <Saos once={true}>
    <h1 class="left-slide">Charts</h1>
  </Saos>
  
</div>
<div class="dexscreener-bg">
  <!-- Has exclusive color hence inline css here -->
  <h2
    class="dexscreener-h2"
    style="margin-top: 10rem; background-image: linear-gradient(135deg, #e0077d 0%, #9c19e0 25%, #3c3cab 75%, #0f8ec7 100%);"
  >
    Pulsechain
  </h2>

  <div class="dexscreener-embed">
    <iframe
      src="https://dexscreener.com/pulsechain/0xE34C1A936AA844dA23fb6e70Aa143e97135691d5?embed=1&theme=dark"
    ></iframe>
  </div>
</div>

<div style="margin-bottom: 5rem;" class="dexscreener-bg">
  <!-- Has exclusive color hence inline css here -->
  <h2
    class="dexscreener-h2"
    style="background-image: linear-gradient(135deg, #292929 0%, #3A3B3C 50%, #414A6B 100%);"
  >
    Ethereum
  </h2>

  <div class="dexscreener-embed">
    <iframe
      src="https://dexscreener.com/ethereum/0xf3f3dccc31235b22d0e5624283e36922c754dc7b?embed=1&theme=dark"
    ></iframe>
  </div>
</div>


<DancingHamster />

<style>
  :root {
    background-image: linear-gradient(135deg, #ffd322 0%, #ffa500 100%);
  }

  h1 {
    font-size: calc(2em + 1vw);
    color: rgba(255, 255, 255, 0.9);
  }

  h2 {
    font-size: calc(1.5em + 0.8vw);
    color: rgba(255, 255, 255, 0.9);
  }

  p {
    font-size: 1.5em;
    color: rgba(255, 255, 255, 0.9);
  }

  .wallpaper-clip-container {
    width: 100%;
    height: 31.5vw;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: flex-start; 
  }

  .wallpaper-image {
    width: 100%;
    height: auto;
  }

  .section-1 {
    text-align: center;
    color: white;
    transition: transform 0.2s ease-out;
    padding: 6rem;
  }

  .red-theme {
    border-radius: 1px;
    border-radius: 2rem 0 2rem 0;
    background-image: linear-gradient(135deg, #d35400 0%, #8e44ad 100%);
    max-width: 80rem;
    width: 95%;
    margin: 0 auto;
    margin-bottom: 10rem;
    text-align: center;
  }

  .no-theme {
    border-radius: 1px;
    padding: 1rem;
    padding-top: 2rem;
    width: 75%;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
    background-image: none;
    color: #332809;
    margin: 0 auto;
  }

  /* This is called yellow theme, because it makes use of the default bg color which is yellow */
  .yellow-theme {
    background: #332809;
  }

  @keyframes slideInFromLeft {
    from {
      transform: translateX(-100%);
      opacity: 0;
    }
    to {
      transform: translateX(0);
      opacity: 1;
    }
  }

  .left-slide {
    opacity: 0;
    transform: translateX(-100%);

    animation-name: slideInFromLeft;
    animation-duration: 1s;
    animation-fill-mode: forwards;
    animation-delay: 0.5s;
  }

  @keyframes slideInFromRight {
    from {
      transform: translateX(100%);
      opacity: 0;
    }
    to {
      transform: translateX(0);
      opacity: 1;
    }
  }

  .right-slide {
    opacity: 0;
    transform: translateX(-100%);

    animation-name: slideInFromRight;
    animation-duration: 1s;
    animation-fill-mode: forwards;
    animation-delay: 0.5s;
  }

  main {
    position: relative;
    z-index: 1;
  }

  .team-members-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    width: 99%;
    margin: 0 auto;
  }

  .buy-container {
    background-image: linear-gradient(135deg, #d3540090 0%, #8e44ad 100%);
    padding-top: calc(5rem + 15vw);
    padding-bottom: calc(5rem + 15vw);
    display: flex;
    flex-direction: column;
    gap: calc(5rem + 5vw);
    align-items: center;
  }

  .dexscreener-h2 {
    text-align: center;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.35);
    color: rgba(255, 255, 255, 0.9);
    width: calc(15rem + 12vw);
    margin: 0 auto;
    padding: 2rem;
    font-size: 3em;
    border-radius: 1px;
  }

  .dexscreener-bg {
    background: linear-gradient(to top, #9561001d 0%, #a16a041b 100%);
    border: 5px dotted;
    border-color: rgba(153, 111, 5, 0.013);
    width: 90%;
    margin: 0 auto;
    padding-top: 5rem;
    margin-top: 10rem;
    border-radius: 1px;
  }

  .dexscreener-embed {
    margin: 0 auto;
    margin-top: 2rem;
    position: relative;
    width: 70%;
    padding-bottom: 155%;
  }

  @media (min-width: 1168px) {
    .buy-container {
      flex-direction: row;
      justify-content: center;
      align-items: center;
    }
  }

  @media (min-width: 1400px) {
    .dexscreener-embed {
      padding-bottom: 55%;
    }
  }
  .dexscreener-embed iframe {
    margin: 0 auto;
    position: absolute;
    width: 100%;
    height: 60%;
    top: 0;
    left: 0;
    border: 0;
  }

  @media (max-width: 600px) {
    .dexscreener-embed {
      padding-bottom: 125%;
      width: 90%;
    }
  }


  @media (max-width: 800px) {
  .section-1{
    padding: 2rem; /* Adjust padding as needed for smaller screens */
  }
  .yellow-theme {
    padding: 4rem;
  }
}

</style>
