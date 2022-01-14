<script>
  export let playerName;
  export let playerScore;

  function increasePlayer1Score() {
    playerScore += 1;
  }
  function decreasePlayer1Score() {
    playerScore -= 1;
    if (playerScore <= 0) {
      playerScore = 0;
    }
  }
</script>

<div>
  <h2 class="center">{playerName}</h2>
  <h3 class="center">{playerScore}</h3>
  <button on:click={increasePlayer1Score}>Up</button>
  <button on:click={decreasePlayer1Score}>Down</button>
</div>

<style>
  .center {
    text-align: center;
  }
</style>
