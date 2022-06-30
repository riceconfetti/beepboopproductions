<script>
    export let currTimeDisplay;
    export let totalTimeDisplay;
    export let progress;
</script>


<div id="time">
    <span id="progress-time">{currTimeDisplay}</span>
    <span id="track-duration">{totalTimeDisplay}</span>
</div>

<div id="progress-bar-cont">
    <span id="bar" style="width: {progress}%"></span>
</div>

<style lang="scss">

</style>