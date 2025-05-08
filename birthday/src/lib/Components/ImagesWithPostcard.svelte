<script lang="ts">
    let { source } = $props()
    let Postcard: HTMLElement
    console.log(source)
</script>

<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_static_element_interactions -->
<div class="container">
    {#if source.source2}
        <div class="card">
            <div class="front">
                <img src={source.source} alt="" />
            </div>
            <div class="back">
                <img src={source.source2} alt="" class="backImage" />
                <p>{source.text}</p>
              <div class="bottom">
                <h4>With Love</h4>
                <h3>{source.name}</h3>
              </div>
            </div>
        </div>
    {:else}
        <div class="card2">
            <div class="front">
                <img src={source.source} alt="" />
            </div>
        </div>
    {/if}
</div>

<style>
  .back p{
    margin-top: 1%;
    margin-left: 10%;
    margin-right: 10%;
    overflow-y: auto;
  }
    .container {
        width: 100%;
        perspective: 800px;
    }
    .bottom{
      display: flex;
      flex-direction: column;
      text-align: right;
      margin-right: 10%;
    }
    .container:hover > .card {
        cursor: pointer;
        transform: rotateY(180deg);
    }
    .card {
        width: 100%;
        position: relative;
        transition: transform 1500ms;
        transform-style: preserve-3d;
    }
    .card2 {
        width: 100%;
        position: relative;
    }
    .backImage {
      margin-top: 3%;
      margin-left: 3%;
        width: 20%;
    }
    .front,
    .back {
        width: 100%;
        backface-visibility: hidden;
    }
    .front img {
        width: 100%;
    }
    .back {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgb(255,255,250);
        transform: rotateY(180deg);
        display: flex;
        flex-direction: column;
    }
</style>
