<script>
  import Content from "../../components/Content.svelte";
  let obj = {
    link: "./images/SolarRoof.jfif",
    name: "Solar Roofs",
    info: "Solar Roof is comprised of both glass solar tiles and steel roofing tiles. Glass solar tiles produce energy, while architectural-grade steel tiles add longevity and corrosion resistance to your roof. Both are durable, strong and engineered for all-weather protection."
  }
</script>

<Content bind:data={obj} />
