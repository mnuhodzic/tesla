<script>
  import Content from "../../components/Content.svelte";
  let obj = {
    link: "./images/ModelX.jfif",
    name: "Model X",
    info: "Model X is built from the ground up as an electric vehicle, with a high-strength architecture and floor-mounted battery pack that enable exceptional occupant protection and low rollover risk."
  }
</script>

<Content bind:data={obj} />
