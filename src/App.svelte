<script>
  import { fade } from "svelte/transition";
  import { cubicOut } from "svelte/easing";
</script>

<style>
  container {
    margin: 5px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: 100%;
    max-width: 600px;
  }
  h1 {
    margin: 5px;
    color: #ffffff;
    font-size: 24px;
    text-align: center;
  }
  hr {
    margin: 0px;
    border: none;
    height: 1px;
    background-color: #cccccc;
    width: 100%;
    display: none;
  }
  p {
    margin: 5px;
  }
  a {
    color: #ff0000;
  }
  #logo {
    height: 50px;
    width: 50px;
  }
  .row {
    display: flex;
    flex-direction: row;
    align-items: center;
	justify-content: center;
	width: 100%;
  }
</style>

<container in:fade={{ duration: 2000, easing: cubicOut }}>
  <div class="row">
    <img id="logo" alt="logo" src="logo.svg" />
    <h1>
      when do i
      <span style="color:#ff0000">die?</span>
    </h1>
  </div>
  <hr />
  <p>
    we're not really sure, but we can make some educated guesses. maybe 20
    years? 10 years? tomorrow?
  </p>
  <p>i'm just trying to make a neat lil death calculator.</p>
  <p>
    feel free to give me suggestions in the meantime:&nbsp;
    <a href="mailto:chris@heythisischris.com">chris@heythisischris.com</a>
  </p>
</container>
