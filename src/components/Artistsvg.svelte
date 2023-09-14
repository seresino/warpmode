<script>
  import { spring } from 'svelte/motion';

  let artists = [
    {name: 'Salome Asega', bio: 'Bio 1...'},
    {name: 'Steven Reneau', bio: 'Bio 2...'},
    {name: 'Kola Heyward-Rotimi', bio: 'Bio 3...'},
    {name: 'Zainab Aliyu', bio: 'Bio 4...'},
    {name: 'Ed-en', bio: 'Bio 5...'},
    {name: 'Jazsalyn', bio: 'Bio 6...'},
    {name: 'Anastasia Warren', bio: 'Bio 7...'},
    {name: 'Fields Harrington', bio: 'Bio 8...'},
    {name: 'Morgan Benjamin', bio: 'Bio 9...'},
    {name: 'Saul William', bio: 'Bio 10...'},
  ];

  let isOpen = false;
  function toggleArtists() {
    isOpen = !isOpen;
    console.log(isOpen)
  }

  let width = spring(0);
  $: if (isOpen) {
    width.set(80);  // Set the spring target to 100
  } else {
    width.set(0);  // Set the spring target to 0
  }


  let displayedBio = "";

  function showBio(bio) {
    displayedBio = bio;
    console.log(bio)
  }

  function hideBio() {
    displayedBio = "";
  }
</script>

<div class="artist-bracket">
  <div class="brackets" on:click={toggleArtists}>
    <svg width="50" height="502" viewBox="0 0 50 502" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M31.72 501H1V1H31.72" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <text transform="matrix(0 -1 1 0 20.0601 318.62)" fill="#FCFCFC" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="24" letter-spacing="0em"><tspan x="0" y="21.124">The Artists</tspan></text>
    </svg>
  </div>
  <div class="artist-container" style="width: {$width}vw;">
    <div class="row">
      {#each artists.slice(0, 5) as artist (artist.name)}
        <svg class="artist" width="200" height="125" viewBox="0 0 250 125" fill="none" xmlns="http://www.w3.org/2000/svg"
          on:mouseenter={()=>showBio(artist.bio)}
          on:mouseleave={hideBio}>
          <circle cx="125" cy="9.16" r="7" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
          <text fill="#FCFCFC" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="24" letter-spacing="0em" x="50%" y="101" dominant-baseline="middle" text-anchor="middle">{artist.name}</text>
        </svg>
      {/each}
    </div>
    <div class="row">
      {#each artists.slice(5, 10) as artist (artist.name)}
        <svg class="artist" width="200" height="125" viewBox="0 0 250 125" fill="none" xmlns="http://www.w3.org/2000/svg"
          on:mouseenter={()=>showBio(artist.bio)}
          on:mouseleave={hideBio}>
          <circle cx="125" cy="9.16" r="7" stroke="white" stroke-width="2.16" stroke-miterlimit="10"/>
          <text fill="#FCFCFC" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="24" letter-spacing="0em" x="50%" y="101" dominant-baseline="middle" text-anchor="middle">{artist.name}</text>
        </svg>
      {/each}
    </div>
  </div>
  <div class="brackets" on:click={toggleArtists}>
    <svg width="32" height="503" viewBox="0 0 32 503" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0.27002 501.62H31V1.62012H0.27002" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
    </svg>
  </div>
</div>

<div class="bio-bracket">
  <div class="brackets" on:click={toggleArtists}>
    <svg width="50" height="502" viewBox="0 0 50 502" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M31.72 501H1V1H31.72" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
      <text transform="matrix(0 -1 1 0 20.0601 318.62)" fill="#FCFCFC" xml:space="preserve" style="white-space: pre" font-family="AUTHENTIC Sans" font-size="24" letter-spacing="0em"><tspan x="0" y="21.124">Bio</tspan></text>
    </svg>
  </div>
  <div class="bio-container" style="width: {$width}vw;">
    <div class="bio">
      {displayedBio}
    </div>
    <div class="socials">
      <a href="">Website</a>
      <a href="">Instagram</a>
      <a href="">Contact</a>
    </div>
  </div>
  <div class="brackets" on:click={toggleArtists}>
    <svg width="32" height="503" viewBox="0 0 32 503" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0.27002 501.62H31V1.62012H0.27002" stroke="white" stroke-width="2" stroke-miterlimit="10"/>
    </svg>
  </div>
</div>

<style>

  .artist-bracket {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    margin-top: 5%;
    margin-bottom: 1%;
  }

  .artist-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .row {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    padding: 1rem;
  }

  .artist {
    text-align: center;
    padding: 20px;
  }

  .artist:hover {
    fill: white;
    font-style: oblique;
  }

  .bio-bracket {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    margin-bottom: 5%;
  }

  .bio-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .bio {
    color: white;
    font-family: AUTHENTIC Sans;
    font-size: 24px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    margin: 20px;
  }

  a {
    display:absolute;
    text-decoration: none;
    color: #FCFCFC;
    font-family: AUTHENTIC Sans;
    font-size: 24px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    margin: 20px;
  }

  .brackets {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }
</style>
