<script>

</script>

<div class="audioPlayer">
    <h1>Tracklist</h1>
    <div class="tracklist">
        <ul>
            <li class="active">
                <span class="trackNumber">1.</span>
                <span class="title">All In</span>
                <span>by</span>
                <span class="artist">Stray Kids</span>
            </li>
            <li>
                <span class="trackNumber">1.</span>
                <span class="title">All In</span>
                <span>by</span>
                <span class="artist">Stray Kids</span>
            </li>
            <li>
                <span class="trackNumber">1.</span>
                <span class="title">All In</span>
                <span>by</span>
                <span class="artist">Stray Kids</span>
            </li>
            <li>
                <span class="trackNumber">1.</span>
                <span class="title">All In</span>
                <span>by</span>
                <span class="artist">Stray Kids</span>
            </li>
        </ul>
    </div>
</div>

<style lang="scss">
    .audioPlayer {
      margin: auto;
      width: 70vw;
      h1 {
        margin-bottom: .2em;
        text-shadow: 2px 2px 0px white;
        font-size: 3em;
        color: black;
      }
    }

    .tracklist {
      font-family: "Akira Expanded";
      max-height: 66vh;
      overflow: auto;
      font-weight: normal;
      letter-spacing: 2px;
      background: rgba(0,0,0, 0.9);
      padding: 0em;
      color: #f9b710;
      ul {
        display: grid;
        padding: 1em;
        margin: 0em;
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
            -webkit-text-stroke: .5px;
          }
        }
        li {
          display: flex;
          padding: 1em;
          align-items: center;
          width: fit-content;
          font-weight: 500;
          text-shadow: 1.5px 1.5px 0px #f9b710;
          color: #fff;
          font-size: 12px;
          gap: 20px;
          .trackNumber {
            font-weight: bold;
            text-shadow: none;
          }
          .title, .artist{
            font-weight: normal;
            text-shadow: none;
            color: #f9b710;
            font-size: 16px;
          }
        }
      }
    }
</style>