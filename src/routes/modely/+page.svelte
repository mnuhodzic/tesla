<script>
  import Content from "../../components/Content.svelte";
  let obj = {
    link: "./images/ModelY.jfif",
    name: "Model Y",
    info: "The Tesla Model Y is a battery electric mid-size crossover SUV built by Tesla, Inc. since 2020. The Model Y is based on the Model 3 sedan platform. It shares an estimated 75 percent of its parts with the Tesla Model 3, which includes a similar interior and exterior design and electric powertrain."
  }
</script>

<Content bind:data={obj} />
