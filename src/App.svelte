<script>
  import PlayerScore from "./PlayerScore.svelte";

  let playerOneComponent;
  let playerOneScore = 0;
  let playerTwoComponent;
  let playerTwoScore = 0;

  // Probablemente necesite algun tipo de estado
  function reset() {
    playerOneScore = 0;
    playerTwoScore = 0;
  }
</script>

<main>
  <h1 class="center">Player Score Counter</h1>
  <PlayerScore bind:playerScore={playerOneScore} playerName="Lenny" />
  <PlayerScore bind:playerScore={playerTwoScore} playerName="Lu" />
  <button on:click={reset} class="contrast outline">RESET</button>
</main>
