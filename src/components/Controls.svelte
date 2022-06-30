<script>
    import { createEventDispatcher} from 'svelte';

    let dispatch = createEventDispatcher();

    const icons = {
        play: "./play-outline.svg",
        pause: "./pause-outline.svg",
        back: "./play-skip-back-outline.svg",
        next: "./play-skip-forward-outline.svg",
        shuffle: "./shuffle-outline.svg",
        repeat: "./repeat-outline.svg"
    }

    export let isPlaying;

</script>

<div id="btn-cont">
    <button id="back" on:click={() => dispatch('back')}>
        <img src={icons.back} alt="back"/>
    </button>
    <button id="play" on:click={() => dispatch('playPause')}>
        <img src={isPlaying ? icons.pause : icons.play}
             alt="play"/>
    </button>
    <button id="next" on:click={() => dispatch('next')}>
        <img src={icons.next} alt="next"/>
    </button>
</div>


<style lang="scss">

</style>