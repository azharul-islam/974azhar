<template>
  <div id="app">
    <div id="nav">
      <div id="brand">
        <span class="moonstone-blue">974</span>AZHAR
      </div>
      <router-link to="/">Home </router-link>
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #294e69;
}
#nav {
  padding: 30px;
  a {
    font-family: 'DisposableDroid BB';
    color: #294e69;
    &.router-link-exact-active {
      color: #E04C55;

    }
  }
}

#brand {
  font-family: 'DisposableDroid BB';
  font-size: 50px;
}

.moonstone-blue {
  color: #5BAFBD
}

a {

  &.router-link-exact-active {
    color: #E04C55;
  }
  &:hover{color: #E04C55;}
}

@font-face {
  font-family: 'DisposableDroid BB_Bold';
  src: url('/assets/fonts/DisposableDroidBB-Bold.woff2') format('woff2'),
  url('/assets/fonts/DisposableDroidBB-Bold.woff') format('woff');
  font-weight: bold;
  font-style: normal;
}

@font-face {
  font-family: 'DisposableDroid BB_Italic';
  src: url('/assets/fonts/DisposableDroidBB-Italic.woff2') format('woff2'),
  url('/assets/fonts/DisposableDroidBB-Italic.woff') format('woff');
  font-weight: normal;
  font-style: italic;
}

@font-face {
  font-family: 'DisposableDroid BB_BoldItalic';
  src: url('/assets/fonts/DisposableDroidBB-BoldItalic.woff2') format('woff2'),
  url('/assets/fonts/DisposableDroidBB-BoldItalic.woff') format('woff');
  font-weight: bold;
  font-style: italic;
}

@font-face {
  font-family: 'DisposableDroid BB';
  src: url('/assets/fonts/DisposableDroidBB.woff2') format('woff2'),
  url('/assets/fonts/DisposableDroidBB.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}


</style>
