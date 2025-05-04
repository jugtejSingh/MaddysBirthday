<script>
  let {source, text} = $props()
</script>
<div>
  <img src={source} alt=""/>
<h4>{text}</h4>
</div>
<style>
  div{
    position: relative;
    height: 100%;
  }
  img{
    width: auto;
    height: 100%;
  }
  h4{
    position: absolute;
    background: white;
    font-size: 2rem;
    top: 10%;
    text-align: center;
    left: 25%;
  }
</style>