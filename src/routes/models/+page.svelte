<script>
  import Content from "../../components/Content.svelte";
  let obj = {
    link: "./images/ModelS.jfif",
    name: "Model S",
    info: "Model S is built from the ground up as an electric vehicle, with a high-strength architecture and floor-mounted battery pack for incredible occupant protection and low rollover risk."
  }
</script>

<Content bind:data={obj} />
