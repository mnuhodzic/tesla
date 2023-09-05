<script>
  import Content from "../../components/Content.svelte";
  let obj = {
    link: "./images/Model3.jfif",
    name: "Model 3",
    info: "Model 3 is fully electric with 333 miles of estimated range, so you never need to visit a gas station again. You can charge at home anytime, or plug in on the road with access to over 45,000 Superchargers worldwide."
}
</script>

<Content bind:data={obj} />
