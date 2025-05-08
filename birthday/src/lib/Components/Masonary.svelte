<script lang="ts">
  import ImagesWithPostcard from "$lib/Components/ImagesWithPostcard.svelte";
  interface Props {
    sources: object[]
    columnInGrids: String
    gap: string;
  }
  let {sources, gap, columnInGrids} :Props = $props()
  const myArray:string[] = $derived(columnInGrids.split(" "));
  let numberOfImages: number = $derived(myArray.length)

  let count = 0
  let sourcesValue :number = 0
  let array: string[][] = [];
  let array2 = $derived.by(() => {
    for (let i = 0; i < numberOfImages; i++){
      array.push([])
    }
      while(sources){
        if (sourcesValue === sources.length){
          break
        }
        if (count === numberOfImages) {
          count = 0
        }
        array[count].push(sources[sourcesValue])
        sourcesValue++
        count++
      }
      return array

    })

</script>
<div class="Masonary" style:grid-template-columns={columnInGrids} style:gap={gap} >
  {#each array2 as arr}
    <div class="Masonary__column" style:gap={gap}>
      {#each arr as source}
        <ImagesWithPostcard source={source} />
      {/each}
    </div>
  {/each}
</div>
<style>
  .Masonary {
    width: 100%;
    height: 100%;
    margin-top: 2rem;
    display: grid;
  }
  .Masonary__column{
    width: 100%;
    display: flex;
    flex-direction: column;
  }
</style>