<template>
  <div id="app">
    <div id="nav">
      <div id="brand">
        <span class="moonstone-blue">974</span>AZHAR
      </div>
      <router-link to="/">/Home </router-link>
      <router-link to="/about">/AboutMe </router-link>
      <router-link to="/about">/Portfolio</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #1c4e6c;
}
#nav {
  padding: 20px;
  a {
    font-family: 'disposabledroid_bbregular';
    font-size: 22px;
    color: #1c4e6c;
    &.router-link-exact-active {
      color: #E04C55;

    }

    &:hover {
      color: #36B1BF;
    }
  }
}

#brand {
  font-family: 'disposabledroid_bbregular';
  font-size: 50px;
}

.moonstone-blue {
  color: #36B1BF
}

a {
text-decoration: none;
  &.router-link-exact-active {
    color: #CA3041;
  }
  &:hover{color: #CA3041;}
}


@font-face {
  font-family: 'disposabledroid_bbbold';
  src: url('./assets/fonts/disposabledroidbb_bld-webfont.woff2') format('woff2'),
  url('./assets/fonts/disposabledroidbb_bld-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}




@font-face {
  font-family: 'disposabledroid_bbbold_italic';
  src: url('./assets/fonts/disposabledroidbb_bldital-webfont.woff2') format('woff2'),
  url('./assets/fonts/disposabledroidbb_bldital-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}




@font-face {
  font-family: 'disposabledroid_bbitalic';
  src: url('./assets/fonts/disposabledroidbb_ital-webfont.woff2') format('woff2'),
  url('./assets/fonts/disposabledroidbb_ital-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}




@font-face {
  font-family: 'disposabledroid_bbregular';
  src: url('./assets/fonts/disposabledroidbb-webfont.woff2') format('woff2'),
  url('./assets/fonts/disposabledroidbb-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;

}

</style>
