<script lang="ts">
    import {innerWidth} from "svelte/reactivity/window";
    import Masonary from "$lib/Components/Masonary.svelte";

    export const source = [
      { source: "/images/maddyAndPeople/image1.jpeg",
      },
      { source: "/images/maddyAndPeople/image2.jpeg",
        text: "There are wayyy too many stories for us together and its kinda crazy looking back youre actually one of the few people who has been there for a lot of my first experiences, i cant think of a single funny moment, cause all of our moments are the most random experiences, from snooping through the walls in ncl and in grenada lmao, from playing random card games while drunk, singing anirudh songs out loud, dancing together, speaking in the weirdest mix of tamil and malayalam in a crowded room when no one could understand us, somehow always my partner in crime, you havent judged me and i only sort of get freaked out by your weird asf demonic laugh and the coolest person to live with, i was supposed to write about one instance but honestly every serious situation becomes funny whenever we talk about it, and somehow i always feel like home around you, even when youre family came to grenada spending time with all of you really meant a lot in many ways, idk if its the cultural similarities maybe that just made it better, youre one of my best friends and someone i consider a sister, thanks for always looking out for me and asking me if i need milk when you go grocery shopping. Love you always nanbi",
        source2: "/images/maddyAndPeople/image2.jpeg",
        name: "Shradha"
      },
      {source: "/images/maddyAndPeople/image3.jpeg",
      },
      {source: "/images/maddyAndPeople/image4.jpeg",
      },
      {source: "/images/maddyAndPeople/image5.jpeg",
      },
      {source: "/images/maddyAndPeople/image6.jpeg",
      },
      {source: "/images/maddyAndPeople/image7.jpeg",
      },
      {source: "/images/maddyAndPeople/image8.jpeg",
      },
      {source: "/images/maddyAndPeople/image9.jpeg",
      },
      {source: "/images/maddyAndPeople/image10.jpeg",
      },
      {source: "/images/maddyAndPeople/image11.jpeg",
      },
      {source: "/images/maddyAndPeople/image12.jpeg",
      },
      {source: "/images/maddyAndPeople/image13.jpeg",
      },
      {source: "/images/maddyAndPeople/image14.jpeg",
      },
      ];

    console.log(source)
    const columnInGrids :string = $derived.by(()=>{
      if(innerWidth.current <= 700 && innerWidth){
        return "1fr 1fr"
      }else if (innerWidth.current <= 1700 && innerWidth.current >= 700) {
        return "1fr 1fr 1fr";
      }
      else{
        return "1fr 1fr 1fr 1fr";
      }
    });
</script>

<div class="Container">
    <Masonary sources={source} columnInGrids={columnInGrids} gap={'1rem'} />
</div>

<style>
    .Container {
      width: 100%;
      background: #e6e6fa;
    }
</style>