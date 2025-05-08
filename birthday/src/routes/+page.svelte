<script lang="ts">
    import BirthdayMessage from '$lib/Components/BirthdayMessage.svelte'
    import Present from '$lib/Components/Present.svelte'
    import ImageGallery from '$lib/Components/ImageGallery.svelte'
    import OurImagesTogether from '$lib/Components/OurImagesTogether.svelte'
</script>

<div class="snapContainer">
    <section class="snapSection birthdaySection">
        <BirthdayMessage />
    </section>

    <section class="snapSection presentsSection">
        <div class="presentsDiv">
            <Present
                width={20}
                angle={2}
                colorOfRibbon={'gold'}
                backgroundR={255}
                backgroundG={112}
                backgroundB={112}
                video="/video/video1.mp4"
            />
            <Present
                width={20}
                angle={-2}
                colorOfRibbon={'pink'}
                backgroundR={255}
                backgroundG={255}
                backgroundB={255}
                video="/video/video2.mp4"
            />
            <Present
                width={10}
                angle={5}
                colorOfRibbon={'lightblue'}
                backgroundR={109}
                backgroundG={0}
                backgroundB={112}
                video="/video/video3.mp4"
            />
            <Present
                width={31}
                angle={-4}
                colorOfRibbon={'brown'}
                backgroundR={50}
                backgroundG={0}
                backgroundB={0}
                video="/video/video5.mp4"
            />
            <Present
                width={18}
                angle={2}
                colorOfRibbon={'gold'}
                backgroundR={150}
                backgroundG={50}
                backgroundB={0}
                video="/video/video6.mp4"
            />
            <Present
                width={25}
                angle={8}
                colorOfRibbon={'lightblue'}
                backgroundR={255}
                backgroundG={0}
                backgroundB={0}
                video="/video/video7.mp4"
            />
            <Present
                width={29}
                angle={0}
                colorOfRibbon={'black'}
                backgroundR={255}
                backgroundG={255}
                backgroundB={255}
                video="/video/video8.mp4"
            />
          <Present
              width={25}
              angle={-9}
              colorOfRibbon={'lightpink'}
              backgroundR={50}
              backgroundG={0}
              backgroundB={0}
              video="/video/video4.mp4"
          />
          <Present
              width={31}
              angle={5}
              colorOfRibbon={'gold'}
              backgroundR={150}
              backgroundG={50}
              backgroundB={0}
              video="/video/video9.mp4"
          />
          <Present
              width={19}
              angle={10}
              colorOfRibbon={'lightblue'}
              backgroundR={109}
              backgroundG={0}
              backgroundB={112}
              video="/video/video10.mp4"
          />
          <Present
              width={31}
              angle={-4}
              colorOfRibbon={'gold'}
              backgroundR={255}
              backgroundG={112}
              backgroundB={112}
              video="/video/video11.mp4"
          />
          <Present
              width={31}
              angle={-4}
              colorOfRibbon={'pink'}
              backgroundR={255}
              backgroundG={255}
              backgroundB={255}
              video="/video/video12.mp4"
          />
          <Present
              width={31}
              angle={-4}
              colorOfRibbon={'beige'}
              backgroundR={80}
              backgroundG={20}
              backgroundB={255}
              video="/video/video13.mp4"
          />
          <Present
              width={31}
              angle={0}
              colorOfRibbon={'lightblue'}
              backgroundR={40}
              backgroundG={170}
              backgroundB={29}
              video="/video/video14.mp4"
          />
        </div>
    </section>
    <section class="snapSection imageGallery">
        <ImageGallery />
    </section>
    <section class="snapSection ourImagesTogether">
        <OurImagesTogether />
    </section>
</div>
<style>
    .ourImagesTogether {
        height: 100%;
      position: relative;
    }
    .snapContainer {
        scroll-snap-type: y proximity;
        overflow-y: auto;
        height: 100%;
        width: 100%;
        position: fixed;
        top: 0;
        left: 0;
    }
    .snapSection {
        scroll-snap-align: start;
        position: relative;
    }

    .birthdaySection {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .presentsSection {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .presentsDiv {
        width: 90vw;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        gap: 2rem;
        padding: 2rem;
    }
    .imageGallery {
        width: 100%;
    }
</style>
