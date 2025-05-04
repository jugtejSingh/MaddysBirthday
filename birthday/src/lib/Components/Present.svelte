<script lang="ts">
    let { width, angle, colorOfRibbon, backgroundR, backgroundG, backgroundB } =
        $props()
    let videoElement: HTMLVideoElement
    async function playVideo() {
      await sleep(200)
      videoElement.play()
    }
    function sleep(ms: number) {
      return new Promise(resolve => setTimeout(resolve, ms))
    }
    function pauseVideo() {
        videoElement.pause()
    }
    if (width <= 10){
      width = 20
    }
</script>

<div
    class="Container"
    style="--width: {width}%; --degrees: {angle}deg;"
    onmouseover={() => playVideo()}
    onfocus={() => playVideo()}
    onmouseout={() => pauseVideo()}
    onblur={() => pauseVideo()}
    role="article">
    <video controls bind:this={videoElement}>
        <source src="/video/cocoa-tea.mp4" type="video/mp4" />
        <track kind="captions" label="English" src="" srclang="en" />
    </video>
    <div
        class="Outside"
        style="--colorOfBackground : rgba({backgroundR},{backgroundG},{backgroundB},1)">
        <div
            class="Horizontal"
            style="--colorOfRibbon : {colorOfRibbon};">

        </div>
        <div class="Vertical" style="--colorOfRibbon : {colorOfRibbon};"></div>
        <img src="/images/bow.png" alt="" class="Ribbon" />
    </div>
</div>

<style>
    .Horizontal {
        background: var(--colorOfRibbon, gold);
        position: absolute;
        width: 13%;
        margin-left: 42%;
        height: 100%;
        z-index: 0;
    }
    .Vertical {
        position: absolute;
        width: 100%;
        height: 20%;
        margin-top: 23%;
        background: var(--colorOfRibbon, gold);
        z-index: 0;
    }
    .Container {
      scroll-snap-align: start;
        margin-left: 2rem;
        width: var(--width, 25%);
        height: 40%;
        transform: rotate3d(0, 0, -100, var(--degrees, 2deg));
        position: relative;
    }
    .Container video {
        width: 100%;
    }
    .Outside {
        content: '';
        position: absolute;
        width: 100%;
        height: 99%;
        top: 0;
        left: 0;
        background: var(--colorOfBackground, rgb(255, 102, 102));
        transform: perspective(200rem) rotateX(0deg); /* Initial */
        transform-origin: top;
        transition: transform 0.8s ease-in-out;
    }
    .Container:hover .Outside {
        transform: perspective(200rem) rotateX(85deg); /* Target on hover */
    }
    @keyframes present-opening {
        0% {
            transform: perspective(200rem) rotateX(0deg);
        }
        100% {
            transform: perspective(200rem) rotateX(85deg);
        }
    }

    .Ribbon {
        position: absolute;
        max-width: 36%;
        top: 26%;
        left: 32%;
    }
</style>
