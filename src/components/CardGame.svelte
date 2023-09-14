<script>
  import { onMount } from 'svelte';
  import { spring } from 'svelte/motion';
  import Bbwwsvg from './Bbwwsvg.svelte';

  let isOpen = false;
  function toggleGame() {
    isOpen = !isOpen;
    console.log(isOpen)
  }

  let width = spring(0);
  $: if (isOpen) {
    width.set(80);  // Set the spring target to 100
  } else {
    width.set(0);  // Set the spring target to 0
  }

  let king = '/images/king_of_hearts2.png';
  let ace = '/images/Playing_card_spade_A.png';
  let queen = '/images/queen_of_diamonds2.png';
  let four = '/images/Playing-Card-PNG-Clipart.png';
  let two = '/images/Playing-Card-PNG-Image.png';

  let cardPack = [
    king,
    ace,
    queen,
    four,
    two
  ];

  let drawnCard = '';

  function drawCard() {
    const randomIndex = Math.floor(Math.random() * cardPack.length);
    drawnCard = cardPack[randomIndex];
  }

  onMount(() => {
    // Automatically draw a card when the component mounts
    drawCard();
  });

</script>

<div class="cardgame-bracket">
  <div class="brackets" on:click={toggleGame}>
    <svg width="50" height="502" viewBox="0 0 50 502" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M31.72 501H1V1H31.72" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      </svg>
    </div>
    <div class="cardgame-container" style="width: {$width}vw;">
      <div class="circle-container">
        <Bbwwsvg />
      </div>
      <div class="card-container">
        <img class="card" src={drawnCard} alt="Drawn Card" />
        <br>
        <h1 on:click={drawCard}>CLICK TO DRAW CARD</h1>
        <!-- <svg width="460" height="32" viewBox="0 0 460 32" fill="none" xmlns="http://www.w3.org/2000/svg" on:click={drawCard}>
          <text fill="#FCFCFC" xml:space="preserve" style="white-space: pre" ><tspan x="-1" y="31.04">CLICK TO DRAW CARD</tspan></text>
        </svg> -->
      </div>
      <div class="circle-container">
        <Bbwwsvg />
      </div>
    </div>
  <div class="brackets" on:click={toggleGame}>
    <svg width="32" height="503" viewBox="0 0 32 503" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0.27002 501.62H31V1.62012H0.27002" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
    </svg>
  </div>
</div>

<style>
  .cardgame-bracket {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .cardgame-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    width: 80vw;
    /* border: 1px dashed #aaa; */
  }

  .circle-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 200px;
    margin: 50px;
    /* border: 1px dashed greenyellow; */
  }

  .card-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-items: center;
    margin: 100px;
    /* border: 1px dashed white; */
  }

  .card {
    width: 250px;
    height: 400px;
  }

  h1 {
    color: white;
    font-family: "AUTHENTIC Sans";
    font-size: 20px;
    font-weight: 600px;
    letter-spacing: 0em;
    text-align: center;
    cursor: pointer;
    user-select: none;
  }

  .brackets {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }


</style>
