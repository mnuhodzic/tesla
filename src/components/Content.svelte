<script>
  import Loader from "./Loader.svelte";

  export let data;

  function preload(src) {
    return new Promise(function(resolve) {
      img = new Image();
      img.onload = resolve;
      img.src = src;
    })
  }
  let img;
  let src = data?.link;
</script>

{#await preload(src)}
  <Loader />
{:then}
  <div class="car_page">
    <img {src} class="car_image">
  </div>
  
  <div class="car_details transform_50">
    <h1 class="model_name">{data.name}</h1>
    <h2 class="model_info">{data.info}</h2>
  </div>
{/await}