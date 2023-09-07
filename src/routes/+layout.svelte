<script>
  import "../app.css";
</script>

<nav class="navbar">
  <!-- logo -->
  <img src="./images/tesla.svg" alt="tesla logo" class="h-6">
  <!-- nav links -->
  <div class="hidden lg:block">
    <a href="/models" class="nav_option">Model S</a>
    <a href="/model3" class="nav_option">Model 3</a>
    <a href="/modelx" class="nav_option">Model X</a>
    <a href="/modely" class="nav_option">Model Y</a>
    <a href="/solarroof" class="nav_option">Solar Roof</a>
    <a href="/solarpanels" class="nav_option">Solar Panels</a>
  </div>
  <!-- external links -->
  <div class="hidden lg:block">
    <a href="https://shop.tesla.com/" class="nav_option">Shop</a>
  </div>
</nav>

<slot />

<svelte:head>
  <title>Tesla</title>
</svelte:head>