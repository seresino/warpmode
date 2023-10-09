<script>
  import { onMount } from 'svelte';
  import { spring } from 'svelte/motion';
  import Bbwwsvg from './Bbwwsvg.svelte';
  import inView from './inView.js'

  let animate = false;
  let isOpen = false;

  let animationOrder = 'forward';  // initial value
  let width = spring(0, {stiffness: 0.05, damping: 0.8});
  $: if (isOpen) {
    width.set(90);  // Set the spring target to 90
  } else {
    width.set(0);  // Set the spring target to 0
  }

  function handleAnimationEnd(event) {
    if (event.propertyName === 'height' && event.target.dataset.bracket === 'right') {
      const elementHeight = event.target.clientHeight;
      if (elementHeight > 100) {
        isOpen = true;
      }
    }
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

<div class="cardgame-bracket"
  use:inView={{ threshold: 0.9}}
  on:enter={() => {
    animationOrder = 'forward';
    animate = true;
    console.log('animate');
    console.log(animate);
  }}
  on:exit={() => {
    animationOrder = 'reverse'
    isOpen = false;
    console.log('is Open');
    console.log(isOpen);
    animate = false;
    console.log('animate');
    console.log(animate);
  }}>

  <div class="shape-left {animationOrder}" class:animate={animate} data-bracket="left"></div>

    <div class="cardgame-container" style="width: {$width}vw;">

      <div class="circle-container">
        <Bbwwsvg />
      </div>

      <div class="card-container">
        <img class="card" src={drawnCard} alt="Drawn Card" />
        <br>
        <h1 on:click={drawCard}>CLICK TO DRAW CARD</h1>
      </div>

      <div class="circle-container">
        <Bbwwsvg />
      </div>

    </div>

  <div class="shape-right {animationOrder}" class:animate={animate} data-bracket="right" on:transitionend={handleAnimationEnd}></div>

</div>

<style>
  .cardgame-bracket {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    width: 95vw;
    height: 95vh;
    overflow: hidden;
  }

  .cardgame-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    width: 80vw;
    height: 80vh;
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

  /* .brackets {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  } */

  .shape-left{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;

    width: 50px;
    height: 100px;
    border: 2px solid white;
    border-right: none;
    background-color: transparent;

    transform-origin: center;
    transform: rotate(-45deg) translateY(17.666%) translateX(-15%);
  }

  .shape-right{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;

    width: 50px;
    height: 100px;
    border: 2px solid white;
    border-left: none;
    background-color: transparent;

    transform-origin: center;
    transform: rotate(-45deg) translateY(-17.666%) translateX(15%);
  }

  .shape-left.forward, .shape-right.forward {
    transition:
        transform 1s,
        height 1s 1s;
  }

  .shape-left.reverse, .shape-right.reverse {
    transition:
        height 1s 1s,
        transform 1s 1s;
  }

  .shape-left.animate {
    transform: rotate(0deg) translateY(0%) translateX(0%);
    height: 80vh;
  }

  .shape-right.animate {
    transform: rotate(0deg) translateY(0%) translateX(0%);
    height: 80vh;
  }

</style>
