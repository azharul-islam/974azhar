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
    font-family: 'disposabledroid_bbregular';
    color: #294e69;
    &.router-link-exact-active {
      color: #E04C55;

    }
  }
}

#brand {
  font-family: 'disposabledroid_bbregular';
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
  font-family: 'disposabledroid_bbbold';
  src: url('/assets/fonts/disposabledroidbb_bld-webfont.woff2') format('woff2'),
  url('/assets/fonts/disposabledroidbb_bld-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}




@font-face {
  font-family: 'disposabledroid_bbbold_italic';
  src: url('/assets/fonts/disposabledroidbb_bldital-webfont.woff2') format('woff2'),
  url('/assets/fonts/disposabledroidbb_bldital-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}




@font-face {
  font-family: 'disposabledroid_bbitalic';
  src: url('/assets/fonts/disposabledroidbb_ital-webfont.woff2') format('woff2'),
  url('/assets/fonts/disposabledroidbb_ital-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}




@font-face {
  font-family: 'disposabledroid_bbregular';
  src: url('/assets/fonts/disposabledroidbb-webfont.woff2') format('woff2'),
  url('/assets/fonts/disposabledroidbb-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}


</style>
