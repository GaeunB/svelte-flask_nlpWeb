<script>
  let introductionText = "";
  let summaryText = "";

  const generateSummary = () => {
    // Your logic to generate the summary goes here
    // For now, let's simply copy the introduction text
    summaryText = introductionText;
  };
</script>

<style>
  /* Additional styling can be added here */
  .container {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    padding: 20px;
  }

  .left-box,
  .right-box {
    width: 45%;
    padding: 20px;
    border: 1px solid #ccc;
    box-sizing: border-box;
  }

  .summary-button {
    margin-top: 10px;
    padding: 8px;
    cursor: pointer;
  }
</style>

<div class="container">
  <div class="left-box">
    <h2>Self Introduction</h2>
    <textarea bind:value={introductionText} placeholder="Enter your self introduction"></textarea>
    <button on:click={generateSummary} class="summary-button">Generate Summary</button>
  </div>

  <div class="right-box">
    <h2>Summary</h2>
    <p>{summaryText}</p>
  </div>
</div>