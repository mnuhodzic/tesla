<script>
  import { goto } from "$app/navigation";
  import { page } from "$app/stores";
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
  const notCar = $page.route.id?.includes('/solarroof') || $page.route.id?.includes('/solarpanels');

  function openTeslaOrderPage() {
    notCar ? goto('https://www.tesla.com/energy/design') : goto(`https://www.tesla.com${$page.route.id}/design#overview`);
  }

  function openTeslaDemoPage() {
    goto(`https://www.tesla.com/drive?selectedModel=${data.name.replace(/\s+/g, '')}`);
  }

  function openTeslaConsultationPage() {
    goto('https://www.tesla.com/solar-virtual-consultations');
  }
</script>

{#await preload(src)}
  <Loader />
{:then}
  <section>
    <div class="car_page">
      <img {src} class="car_image">
    </div>
    
    <div class="car_details transform_50">
      <h1 class="model_name">{data.name}</h1>
      <h2 class="model_info hidden lg:block">{data.info}</h2>
    </div>
  
    <div class="car_buttons transform_50" >
      <button class="btn" on:click={openTeslaOrderPage}>Order Now</button>
      {#if notCar}
        <button class="btn demo" on:click={openTeslaConsultationPage}>Consultation</button>
        {:else}
        <button class="btn demo" on:click={openTeslaDemoPage}>Demo drive</button>
      {/if}
    </div>
  </section>
{/await}