<script>
    // Define the URL you want to navigate to
    const url = "https://app.uniswap.org/tokens/ethereum/0x54f667db585b7b10347429c72c36c8b59ab441cb";
    import PulsechainLogo from '../assets/ethereum_logo.png';
    
    // Function to handle click event
    function navigate() {
        window.location.href = url;
    }
</script>

<style>
    .buy-now-button {
        background-image: linear-gradient(135deg, #FFD322 0%, #FFA500 100%);
        color: #332809;
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
        gap: 10px;
    }

    .buy-now-button img {
        width: 34px; 
        height: auto;
        margin-right: auto; /* Pushes the text towards the right */
    }

    .buy-now-button:hover {
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.25);
        transform: rotate(5deg);
    }
</style>

<button class="buy-now-button" on:click={navigate}>
    <img src={PulsechainLogo} alt="Pulsechain Logo">
    Buy now
</button>
