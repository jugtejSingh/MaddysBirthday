<script>
  let {source} = $props()
</script>
<img src={source} alt="" />
<style>
  img{
    position: absolute;
    width: var(--width, 10%);
    left: var(--left,0);
    top: var(--top,0);
    transform: rotate(var(--degree,0));
  }
</style>