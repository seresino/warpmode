<script>
  import { onMount } from 'svelte';
  import CardGame from '../../components/CardGame.svelte';
  import OrbitSVG from '../../components/Orbitsvg.svelte';
	import Bbwwsvg from '../../components/Bbwwsvg.svelte';
  import Artistsvg from '../../components/Artistsvg.svelte';
  import { spring } from 'svelte/motion';
  import { fly } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';
  import { slide } from 'svelte/transition';

</script>

<div class="page">

  <div class="cardgame-bracket">
    <div class="brackets">
      <svg width="50" height="502" viewBox="0 0 50 502" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M31.72 501H1V1H31.72" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
        </svg>
      </div>
      <div class="cardgame-container">
        <div class="circle-container">
          <Bbwwsvg />
        </div>
        <div class="card-container">
          <CardGame />
        </div>
        <div class="circle-container">
          <Bbwwsvg />
        </div>
      </div>
    <div class="brackets">
      <svg width="32" height="503" viewBox="0 0 32 503" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M0.27002 501.62H31V1.62012H0.27002" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      </svg>
    </div>
  </div>

  <OrbitSVG />

  <Artistsvg />

</div>

<style>
  .page {
    background-color: black;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
  }

  .cardgame-bracket {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
  }

  .cardgame-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    width: 80vw;
    border: 1px dashed #aaa;
  }

  .circle-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 200px;
    margin: 50px;
    border: 1px dashed greenyellow;
  }

  .card-container {
    margin: 100px;
    border: 1px dashed white;
  }

  .brackets {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }

</style>

