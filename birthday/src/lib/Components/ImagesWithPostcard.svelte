<script lang="ts">
    let { source } = $props()
    let Postcard: HTMLElement
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
                <h4>With Love</h4>
                <h3>{source.name}</h3>
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
    .container {
        width: 100%;
        perspective: 800px;
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
        background-color: #3a3a3a;
        transform: rotateY(180deg);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>
