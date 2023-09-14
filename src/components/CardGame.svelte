<script>
  import { onMount } from 'svelte';

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

<div class="box">
  <img class="card" src={drawnCard} alt="Drawn Card" />
  <br>
  <h1 on:click={drawCard}>CLICK TO DRAW CARD</h1>
  <!-- <svg width="460" height="32" viewBox="0 0 460 32" fill="none" xmlns="http://www.w3.org/2000/svg" on:click={drawCard}>
    <text fill="#FCFCFC" xml:space="preserve" style="white-space: pre" ><tspan x="-1" y="31.04">CLICK TO DRAW CARD</tspan></text>
  </svg> -->
</div>

<style>
  h1 {
    color: white;
    font-family: "AUTHENTIC Sans";
    font-size: 20px;
    font-weight: 600px;
    letter-spacing: 0em;
    text-align: center;
  }

  .card {
    width: 250px;
  }

  .box {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-items: center;
  }
</style>
