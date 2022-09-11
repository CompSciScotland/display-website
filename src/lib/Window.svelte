<script>
  import Drive from "./Drive.svelte";
  import ButtonGroup from "./ButtonGroup.svelte";
  let source;
  function handleNewSource(event) {
		//alert(event.detail.text);
        source = event.detail.source
	}
</script>

<ButtonGroup on:message={handleNewSource}/>
<div class="mockup-window border bg-neutral-content w-full">
<Drive source={source}/>
</div>
