<script>
  let current = "early";
</script>

<div class="btn-group mb-3">
  <button
    class:btn-active={current === "early"} class="btn"
    on:click={() => (current = "early")}>Early Levels</button
  >
  <button
  class:btn-active={current === "first"} class="btn"
  on:click={() => (current = "first")}
    >First Level</button
  >
  <button
  class:btn-active={current === "second"} class="btn"
  on:click={() => (current = "second")}>Second Level</button
  >
  <button
    class:btn-active={current === "t/f"} class="btn"
    on:click={() => (current = "t/f")}>Third/Fourth Level</button
  >
  <button
    class:btn-active={current === "senior"} class="btn"
    on:click={() => (current = "senior")}>Senior Level</button
  >
</div>
