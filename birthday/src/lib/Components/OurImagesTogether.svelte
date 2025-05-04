<script lang="ts">
import TheDayOf from "$lib/Components/TheDayOf.svelte";
import {onMount} from "svelte";

let container :HTMLDivElement;

function autoScroll() {
  container.scrollBy(0, 100); // Scroll down by 100 pixels
  setTimeout(autoScroll, 1000); // Repeat after 1 second
}
onMount(() => {
  autoScroll();
})

</script>
<div class="Container" bind:this={container}>
  <TheDayOf source="/images/theDay/image0.jpg" text="The day of diwali bash" />
  <TheDayOf source="/images/theDay/image1.jpg" text="The day we took a spontanous trip to durham" />
  <TheDayOf source="/images/theDay/image2.jpg" text="The day of eid(i think)" />
  <TheDayOf source="/images/theDay/image3.jpg" text="The day of your birthday, morning" />
  <TheDayOf source="/images/theDay/image4.jpg" text="The day of your birthday, evening" />
  <TheDayOf source="/images/theDay/image5.jpg" text="The day we went prickly bay and i puked" />
  <TheDayOf source="/images/theDay/image6.jpg" text="The day we had stags and strawberry coladas" />
  <TheDayOf source="/images/theDay/image7.jpg" text="The day we did nothing but study(good students)" />
  <TheDayOf source="/images/theDay/image8.jpg" text="The day of shradhas birthday" />
  <TheDayOf source="/images/theDay/image9.jpg" text="The day we went on a bougie date" />
  <TheDayOf source="/images/theDay/image10.jpg" text="The day we found out how good cocoa tea is" />
  <TheDayOf source="/images/theDay/image11.jpg" text="The day we spontaneously went to the beach" />
  <TheDayOf source="/images/theDay/image12.jpg" text="The day of something in manor bank lol" />
  <TheDayOf source="/images/theDay/image13.jpg" text="The day of multicultural" />
  <TheDayOf source="/images/theDay/image14.jpg" text="The day we were in london together" />
  <TheDayOf source="/images/theDay/image15.jpg" text="The day you were so highhh" />
  <TheDayOf source="/images/theDay/image16.jpg" text="The day of med gala" />
  <TheDayOf source="/images/theDay/image17.jpg" text="this is just a cool picture" />
  <TheDayOf source="/images/theDay/image18.jpg" text="The day you became a horse" />
  <TheDayOf source="/images/theDay/image19.jpg" text="The day we went clubbing" />
  <TheDayOf source="/images/theDay/image20.jpg" text="The day we went bbc and swam" />
  <TheDayOf source="/images/theDay/image21.jpg" text="this is another cool picture lol" />
</div>
<style>
  .Container{
    display: flex;
    overflow-x: scroll;
    flex-direction: row;
    width: 100%;
    height: 100%;
  }
  .ImageContainer{
    width: 33%;
    height: 100%;
  }
</style>