<script>
  import { createEventDispatcher } from "svelte";
  let current = "early";
  let sources = [
    "https://drive.google.com/embeddedfolderview?id=1nkbDuznngOXDBZULPTV-xi6-5vP9a7A4#list",
    "https://drive.google.com/embeddedfolderview?id=1vTVJgNXIJcXqVdbjV40B_WQKbmCJVV1T#list",
    "https://drive.google.com/embeddedfolderview?id=1HSsHZqH31r0zdAMh_0AomUCYxlMN8pgV#list",
    "https://drive.google.com/embeddedfolderview?id=1WqTTLC0TD8iOjyPnumlb9jgf8JZT0cgd#list",
    "https://drive.google.com/embeddedfolderview?id=1U5RS3-MhupcL1zJHPj-BECFyu5GvkECz#list",
  ];
  const dispatch = createEventDispatcher();

  function updateIframe(source) {
    dispatch("message", {
      source: source,
    });
  }
</script>

<div class="btn-group mb-3">
  <button
    class:btn-active={current === "early"}
    class="btn"
    on:click={() => (current = "early")}
    on:click={() => updateIframe(sources[0])}>Early Levels</button
  >
  <button
    class:btn-active={current === "first"}
    class="btn"
    on:click={() => (current = "first")}
    on:click={() => updateIframe(sources[1])}>First Level</button
  >
  <button
    class:btn-active={current === "second"}
    class="btn"
    on:click={() => (current = "second")}
    on:click={() => updateIframe(sources[2])}>Second Level</button
  >
  <button
    class:btn-active={current === "t/f"}
    class="btn"
    on:click={() => (current = "t/f")}
    on:click={() => updateIframe(sources[3])}>Third/Fourth Level</button
  >
  <button
    class:btn-active={current === "senior"}
    class="btn"
    on:click={() => (current = "senior")}
    on:click={() => updateIframe(sources[4])}>Senior Level</button
  >
</div>
