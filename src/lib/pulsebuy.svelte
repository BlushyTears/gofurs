<script>
    // Define the URL you want to navigate to
    const url = "https://swap.hedron.pro/#/swap?exactField=output&exactAmount=1&outputCurrency=0x54f667dB585b7B10347429C72c36c8B59aB441cb";
    import PulsechainLogo from '../assets/pulsechain_logo.png';
    
    // Function to handle click event
    function navigate() {
        window.location.href = url;
    }
</script>

<style>
    .buy-now-button {
        background-image: linear-gradient(135deg, #FFD322 0%, #FFA500 100%);
        color: rgba(0,0,0, 0.8);
        padding: 40px 80px;
        border: none;
        cursor: pointer;
        border-radius: 1px;
        font-size: 3em;
        display: flex;
        align-items: center;
        transition: 0.1s ease-in-out;
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.15);
        min-width: 20rem;
    }

    .buy-now-button img {
        width: 64px; 
        height: auto;
    }

    .buy-now-button:hover {
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.25);
        transform: rotate(-5deg);
    }

</style>

<button class="buy-now-button" on:click={navigate}>
    <img src={PulsechainLogo} alt="Pulsechain Logo">
    Buy now
</button>
