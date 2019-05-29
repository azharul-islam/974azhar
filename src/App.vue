<template>
    <div id="app">
        <div id="nav">
            <div id="brand">
                <span class="moonstone-blue">974</span>AZHAR
            </div>
            <router-link to="/">/Blog</router-link>
            <router-link to="/about">/AboutMe</router-link>
            <router-link to="/portfolio">/Portfolio</router-link>
        </div>
        <router-view/>
    </div>
</template>


<style lang="scss">

    $color-bg: rgba(28, 78, 108, 0.07);
    $color-dark: #1c4e6c;
    $color-light: #36B1BF;

    #app {
        font-family: Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: $color-dark;
    }

    .container {
        margin: 0px 10px 10px 10px;
        background-color: white;
        border: 3px solid $color-dark;
        padding: 18px;
    }


    body {
        margin: 0px;
        background-color: #F4F4F4;
        background-image: linear-gradient(
                        45deg,
                        $color-bg 25%,
                        transparent 25%,
                        transparent 75%,
                        $color-bg 75%,
                        $color-bg
        ),
        linear-gradient(
                        -45deg,
                        $color-bg 25%,
                        transparent 25%,
                        transparent 75%,
                        $color-bg 75%,
                        $color-bg
        );
        background-size: 60px 60px;
        background-position: 0 0;
        animation: slide 4s infinite linear;
    }

    @keyframes slide {
        from {
            background-position: 0 0;
        }

        to {
            background-position: -120px 60px;
        }
    }

    h1 {
        font-family: 'disposabledroid_bbbold';
    }

    #nav {
        position: fixed;
        /*width: 100%;*/
        top: 10px;
        left: 10px;
        right: 10px;
        padding: 18px 18px 8px 18px;
        border: 3px solid $color-dark;
        box-shadow: 0.2rem 0.2rem 0 $color-dark;
        background-color: white;

        a {
            padding: 10px 26px 10px 0;
            font-family: 'disposabledroid_bbbold';
            font-size: 24px;
            color: $color-dark;
            text-decoration: none;
            display: inline-block;

            &:last-child {
                padding-right: 10px;
            }

            &:visited {
                color: $color-dark;
            }

            &:hover {
                color: #36B1BF;
            }

            &:active {
                color: $color-dark;
            }

            &.router-link-exact-active {
                color: #CA3041;
                pointer-events: none;
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
        -webkit-tap-highlight-color: transparent;
        color: $color-dark;

        &.router-link-exact-active {
            color: #CA3041;
        }

        &:hover {
            color: #36B1BF;
        }
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
