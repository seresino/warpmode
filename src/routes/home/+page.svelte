<script>
  import CardGame from '../../components/CardGame.svelte';
  import OrbitSVG from '../../components/Orbitsvg.svelte';
	import Bbwwsvg from '../../components/Bbwwsvg.svelte';
  import Artistsvg from '../../components/Artistsvg.svelte';
	import Orbitsvg from '../../components/Orbitsvg.svelte';

</script>

<div class="page">
  <section>
    <CardGame/>
  </section>
  <section>
    <Orbitsvg/>
  </section>
  <section>
    <Artistsvg/>
  </section>
</div>

<style>
  .page {
    scroll-snap-type: y mandatory;
    scroll-snap-type: mandatory;
    -webkit-overflow-scrolling: touch;
    display: flex;
    height: 100vh;
    flex-direction: column;
    overflow-y: scroll;
  }
  section {
    position: relative;
    width: 100%;
    min-height: 100%;


    background-color: black;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    /* height: 100vh; */
    /* width: 100vw; */
    scroll-snap-align: start;
    scroll-snap-stop: always;
  }

</style>

