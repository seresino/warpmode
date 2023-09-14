<script>
  import { onMount } from 'svelte';
  import AnimatedSVG from '../components/Landingsvg.svelte';

  let password = '';
  let errorMessage = '';

  function handleSubmit() {
    const correctPassword = 'yourpassword';

    if (password === correctPassword) {
      window.location.href = "/home";
    } else {
      errorMessage = 'Incorrect password. Please try again.';
    }
  }

  onMount(() => {
    // Optional: Perform any initialization logic when the component is mounted
  });
</script>

<div class="page">
  <form class="password-box" on:submit|preventDefault={handleSubmit}>
    <label for="password">Password:</label>
    <input type="password" id="password" bind:value={password}>
    <p class="error-message">{errorMessage}</p>
    <button class="submit" type="submit">Submit</button>
  </form>

  <AnimatedSVG />
</div>

<style>
  :global(body) {
    background-color: black;
  }

  .password-box {
    width: 300px;
    margin: 100px auto;
    position: absolute;
    padding: 20px;
    border: 1px solid #ccc;
    text-align: center;
  }

  .submit {
    padding: 5px 10px;
  }

  .error-message {
    color: red;
  }

  .page {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
  }

</style>
