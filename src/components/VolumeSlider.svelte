<script>
    export let vol;
</script>

<div class="slidecontainer">
    <label for="volume-slider">0</label>

    <input id="volume-slider"
           class="slider"
           type="range"
           min="0"
           max="100"
           step="1"
           name="volume"
           bind:value={vol}
           on:input
    >

    <label for="volume-slider">{vol}</label>
</div>

<style lang="scss">

</style>