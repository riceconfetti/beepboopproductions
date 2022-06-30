<script>
    import Playlist from "../components/Playlist.svelte";
    export let audioData;
</script>

<div class="audioPlayer">
    <h1>Tracklist</h1>

    <div class="player">
        <div class="controls">
            <button id="back" >
                <img src="./play-skip-back-outline.svg" alt="back"/>
            </button>
            <button id="play">
                <img src="./play-outline.svg" alt="play"/>
            </button>
            <button id="forward">
                <img src="./play-skip-forward-outline.svg" alt="skip"/>
            </button>
            <button id="shuffle">
                <img src="./shuffle-outline.svg" alt="shuffle"/>
            </button>
            <button id="repeat">
                <img src="./repeat-outline.svg" alt="repeat"/>
            </button>
        </div>

        <div class="progress-bar">
            <span id="progress-time">0:00</span>
            <div id="progress-bar-cont">
                <span id="bar" style="width:30%" ></span>
            </div>
            <span id="track-duration">0:27</span>
        </div>
    </div>

    <Playlist {audioData}/>
</div>

<style lang="scss">
    .audioPlayer {
      margin: auto;
      width: 70vw;
      .player {
        padding: 1rem;
        display: flex;
        background: #f9b710;
        border: 2px solid black;
        margin-bottom: 2rem;
        box-shadow: 8px 8px 0px black;
        gap: 3rem;
        font-family: "Akira Expanded";
        font-size: .8rem;
        align-items: center;
        color:black;
        .controls {
          display: flex;
          gap: 5px;
          button {
            border: none;
            background-color: rgba(0, 0, 0, 0);
            img {
              color: black;
              width: 1.3rem;
            }
          }
        }
        .progress-bar {
          width: 100%;
          display: flex;
          gap: 1rem;
          #progress-bar-cont {
            width: 100%;
            border: 1px solid black;
            background-color: rgba(0,0,0,0);
            #bar {
              display: block;
              height: 100%;
              background: black;
            }
          }
        }

      }
      h1 {
        margin:0;
        margin-bottom: .2em;
        text-shadow: 2px 2px 0px white;
        font-size: 3em;
        color: black;
      }
    }
</style>