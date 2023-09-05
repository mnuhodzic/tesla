<script>
  import Content from "../../components/Content.svelte";
  let obj = {
    link: "./images/SolarPanels.jfif",
    name: "Solar Panels",
    info: "Solar panels can save you money by using space on your roof to produce sustainable energy right from your home. Tesla solar panels have a low-profile design and no visible mounting hardware."
}
</script>

<Content bind:data={obj} />
