<template>
    <div id="app">
        <div id="nav" v-scroll="handleScroll" :class="{minimized: isMinimized, 'nav-menu-active': isMobileMenuActive}">
            <div id="brand">
                <span class="moonstone-blue">974</span>AZHAR
            </div>
            <router-link to="/" replace>/Blog</router-link>
            <router-link to="/about" replace>/AboutMe</router-link>
            <router-link to="/portfolio" replace>/Portfolio</router-link>

            <div class="menu-button" :class="{change: isMobileMenuActive, 'menu-visible': isMinimized}" @click.prevent="toggleMobileMenu">
                <div class="bar1"></div>
                <div class="bar2"></div>
            </div>
        </div>
        <router-view/>
    </div>
</template>
<script>

    export default {
        name: 'App',
        props: {},
        data: function () {
            return {
                isMinimized: false,
                isMobileMenuActive: false,
            }
        },
        methods: {
            handleScroll: function () {
                if (window.scrollY > 130) {
                    this.isMinimized = true;
                }
                if(window.scrollY < 130) {
                    this.isMinimized = false
                }
            },
            toggleMobileMenu: function () {
                this.isMobileMenuActive = !this.isMobileMenuActive;
            }

        }

    }
</script>

<style lang="scss">

    $color-bg: rgba(28, 78, 108, 0.07);
    $color-dark: #1c4e6c;
    $color-light: #36B1BF;
    $color-accent: #CA3041;

    #app {
        font-family: Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: $color-dark;
    }

    .container {
        margin: 0px 10px 10px 10px;
        background-color: white;
        border: 2px solid $color-dark;
        user-select: none;
        /*max-width: 1000px;*/
    }

    .minimized {

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
        background-size: 80px 80px;
        background-position: 0 0;
        animation: slide 4s infinite linear;
    }

    img {
        border: 2px solid $color-dark;
    }

    @keyframes slide {
        from {
            background-position: 0 0;
        }

        to {
            background-position: -120px 60px;
        }
    }

    h1, h2, h3, h4, h5, h6 {
        font-family: 'disposabledroid_bbbold';
    }

    #nav {
        position: fixed;
        z-index: 1000;
        top: 10px;
        left: 10px;
        right: 10px;
        overflow: hidden;
        padding: 14px 14px 4px 14px;
        border: 2px solid $color-dark;
        box-shadow: 0.22rem 0.22rem 0 $color-dark;
        background-color: white;
        height: 70px;
        transition: height .5s cubic-bezier(0.52, 0.16, 0.24, 1);

        a {
            padding: 12px 18px 10px 0;
            font-family: 'disposabledroid_bbbold';
            font-size: 20px;
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
                color: $color-light;
            }

            &:active {
                color: $color-dark;
            }

            &.router-link-exact-active {
                color: #CA3041;
                pointer-events: none;
            }

        }

        &.minimized{
            height: 38px;
        }
    }

    #nav.nav-menu-active {
        height: 70px;
    }

    #brand {
        font-family: 'disposabledroid_bbregular';
        font-size: 36px;
    }

    .moonstone-blue {
        color: $color-light
    }

    a {
        -webkit-tap-highlight-color: transparent;
        color: $color-dark;

        &.router-link-exact-active {
            color: #CA3041;
        }

        &:hover {
            color: $color-light;
        }
    }

    .menu-button {
        position: absolute;
        top: 0;
        right: 0;
        opacity: 0;
        pointer-events: none;
        cursor: pointer;
        -webkit-tap-highlight-color: transparent;
        padding: 15px 18px 20px 18px;
        justify-self: start;
        transition: opacity 0.2s cubic-bezier(0.645, 0.045, 0.355, 1);

        div {
            width: 22px;
            height: 2px;
            background-color: $color-dark;
            margin: 7px 0;
            transition: transform .1596s cubic-bezier(0.52, 0.16, 0.52, 0.84) .1008s;
            transform: none;
        }
    }

    .menu-button.menu-visible {
        opacity: 1;
        pointer-events: auto;
        transform: scaleY(1);

    }

    .change .bar1 {
        transform: rotate(-45deg) translate(-2.5px, 4px);
    }

    .change .bar2 {
        transform: rotate(45deg) translate(-2.5px, -4px);
    }


    .swiper-pagination-bullet {
        width: 6px !important;
        height: 6px !important;
        background: white !important;
        opacity: 1 !important;
        border: 1px solid $color-dark !important;
    }

    .swiper-pagination-bullet-active {
        background-color: $color-dark !important;
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
