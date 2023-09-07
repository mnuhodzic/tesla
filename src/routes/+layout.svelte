<script>
  import "../app.css";
  let showMobMenu = false;
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
  <!-- mobile navigation -->
  <div class="lg:hidden">
    <button class="navbar_mob" on:click={() => showMobMenu=!showMobMenu}>
      <svg class="block h-5 w-5 fill-current" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
        <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
      </svg>
    </button>
  </div>
</nav>

{#if showMobMenu}
<div class="nav_menu_mob">
  <div class="nav_backdrop_mob" on:click={() => showMobMenu=!showMobMenu}></div>
  <nav class="fixed top-0 left-0 bottom-0 flex flex-col w-5/6 max-w-sm py-6 px-6 bg-white border-r overflow-y-auto">
    <ul>
      <li class="mb-1">
        <a href="/models" class="nav_option_mob">Model S</a>
      </li>
      <li class="mb-1">
        <a href="/model3" class="nav_option_mob">Model 3</a>
      </li>
      <li class="mb-1">
        <a href="/modelx" class="nav_option_mob">Model X</a>
      </li>
      <li class="mb-1">
        <a href="/modely" class="nav_option_mob">Model Y</a>
      </li>
      <li class="mb-1">
        <a href="/solarroof" class="nav_option_mob">Solar Roof</a>
      </li>
      <li class="mb-1">
        <a href="/solarpanels" class="nav_option_mob">Solar Panels</a>
      </li>
      <li class="mb-1">
        <a href="https://shop.tesla.com/" class="nav_option_mob">Shop</a>
      </li>
    </ul>
  </nav>
</div>
{/if}

<slot />

<svelte:head>
  <title>Tesla</title>
</svelte:head>