<script lang="ts">
    import {innerWidth} from "svelte/reactivity/window";
    import Masonary from "$lib/Components/Masonary.svelte";

    export const source = [
      { source: "/images/maddyAndPeople/image1.jpeg",
      },
      { source: "/images/maddyAndPeople/image2.jpeg",
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