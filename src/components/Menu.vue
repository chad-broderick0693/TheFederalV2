<template>
  <div id="menu-page">
    <div class="menu-about">
      The Federal Coffee House of Mowrystown, Ohio proudly serves
      ethically-sourced coffee roasted locally in Cincinnati, Ohio by the fine
      roasters of
      <a href="http://www.coffee-emporium.com" target="_blank"
        >Coffee Emporium</a
      >.
    </div>
    <div class="menu">
      <ul class="menu-list coffee">
        <li class="list-header">Coffee:</li>
        <li class="list-item">House Coffee</li>
        <li class="list-item">Seasonal Coffee</li>
      </ul>
      <ul class="menu-list espresso">
        <li class="list-header">Espresso:</li>
        <li class="list-item">Cappuccino</li>
        <li class="list-item">Latte</li>
        <li class="list-item">Macchiato</li>
        <li class="list-item">Frappe</li>
        <li class="list-item">Espresso</li>
        <li class="list-item">Americano</li>
        <li class="list-item">Cortado</li>
        <li class="list-item">Red Eye</li>
      </ul>
      <ul class="menu-list">
        <li class="list-header">Tea:</li>
        <li class="list-item">Earl Grey</li>
        <li class="list-item">Green</li>
        <li class="list-item">Spiced Chai</li>
      </ul>
      <ul class="menu-list">
        <li class="list-header">Other:</li>
        <li class="list-item">Hot Cocoa</li>
      </ul>
      <ul class="menu-list baked-goods">
        <li class="list-header">Baked Goods:</li>
        <li class="list-item">Coming soon!</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Menu",
};
</script>

<style>
@font-face {
  font-family: AboutMenuFont;
  src: url("../fonts/IMFellDoublePica-Regular.ttf");
}

#menu-page {
  width: 50vw;
  display: grid;
  grid-template-rows: 1fr auto;
  grid-gap: 4rem;
  margin: auto;
}

.menu-about {
  font-family: AboutMenuFont;
  width: 53vw;
  height: auto;
  font-size: 2.5rem;
  margin: auto;
  grid-row-start: 1;
  grid-row-end: 2;
}

a,
a:visited {
  color: inherit;
}

.menu {
  grid-row-start: 2;
  grid-row-end: 3;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1.5fr;
}

.list-header {
  font-size: 3.5rem;
  cursor: default;
}

.list-item {
  display: block;
  font-family: sans-serif;
  font-size: 2rem;
  cursor: default;
  margin-top: 0.7rem;
  margin-bottom: 0.7rem;
}

@media only screen and (max-width: 700px) {
  #menu-page {
    width: auto;
  }

  .menu {
    grid-template-columns: auto auto;
    grid-template-rows: auto auto auto;
    justify-content: center;
  }

  .menu-about {
    width: 95vw;
    text-align: justify;
  }

  .espresso {
    grid-column-start: 1;
    grid-column-end: 2;
  }

  .coffee {
    grid-column-start: 2;
    grid-column-end: 3;
    grid-row-start: 1;
    grid-row-end: 2;
  }

  .baked-goods {
    grid-column-start: 1;
    grid-column-end: 3;
  }
}
</style>
