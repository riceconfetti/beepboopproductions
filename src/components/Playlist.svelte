<script>
    export let audioData;
</script>

<div class="playlist">
    <ul>
        {#each audioData as track, i}
            <li data-track-id = {i} on:click>
                <span class="trackNumber">{i+1}.</span>
                <span class="title">{track.name}</span>
                <span>by</span>
                <span class="artist">{track.artist}</span>
            </li>
        {:else}
            <li>No Tracks Found</li>
        {/each}
    </ul>
</div>


<style lang="scss">
  .playlist {
    font-family: "Akira Expanded", sans-serif;
    max-height: 64vh;
    overflow: auto;
    font-weight: normal;
    letter-spacing: 2px;
    background: rgba(0,0,0, 0.9);
    padding: 0;
    color: #f9b710;
    ul {
      display: grid;
      padding: 1em;
      margin: 0;
      grid-template-columns: auto;
      width: auto;
      li.active {
        background-color: #f9b710;
        font-weight: bold;
        width: auto;
        color:black;
        .title, .artist{
          color: black;
          font-weight:500;
        }
      }
      li {
        display: flex;
        padding: 1em;
        align-items: center;
        width: fit-content;
        font-weight: 500;
        text-shadow: 1.5px 1.5px 0 #f9b710;
        color: #fff;
        font-size: 10px;
        gap: 20px;
        .trackNumber {
          font-weight: bold;
          text-shadow: none;
        }
        .title, .artist{
          font-weight: normal;
          text-shadow: none;
          color: #f9b710;
          font-size: 14px;
        }
      }
    }
  }
</style>