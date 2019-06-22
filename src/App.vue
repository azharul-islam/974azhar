<template>
    <div id="app">
        <div class="nav-container">
            <div id="brand">
                <span class="moonstone-blue">974</span><span>A</span><span>Z</span><span>H</span><span>A</span><span>R</span>
            </div>
            <nav :class="{minimized: isMinimized, 'nav-menu-active': isMobileMenuActive}">
                <router-link to="/" replace>Blog</router-link>
                <router-link to="/about" replace style="margin-bottom: 27px;">About Me</router-link>
                <router-link to="/portfolio" replace>Work</router-link>

            </nav>
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
                if (window.scrollY < 130) {
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
    $color-primary: #3a77d3;
    $color-dark: #1c4e6c;
    $color-light: #3bc2d1;
    $color-accent: #f23c50;

    #app {
        padding: 20px 0 0 0;
        font-family: Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: $color-dark;
        display: grid;
        grid-template-columns: 200px 1fr;
        grid-template-areas: "nav content";
    }

    .container {
        margin: 0px 10px 10px 10px;
        background-color: white;
        user-select: none;
        /*max-width: 1000px;*/
    }


    body {
        margin: 0px;
        background-color: #efefef;
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
        font-family: 'inria_sansbold';
    }

    a {
        box-shadow: 0 2px 0 0 currentColor;
        color: $color-primary;
        text-decoration: none;
        transition: color .2s cubic-bezier(.47, 0, .74, .71), font-size .2s cubic-bezier(.47, 0, .74, .71);
        /*-webkit-tap-highlight-color: transparent;*/

        &:hover {
            color: $color-light;
        }

        &:active {
            color: $color-primary;
        }

        &:focus {
            color: $color-primary;
        }
    }

    .nav-container {
        grid-area: nav;
        display: flex;
        align-items: flex-end;
        flex-direction: column;
        padding: 36px 0px 45px 0px;
    }

    nav {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        transition: height .5s cubic-bezier(0.52, 0.16, 0.24, 1);

        a {
            user-select: none;
            margin: 8px 0px;
            font-family: 'inria_sansbold';
            font-weight: bold;
            font-size: 22px;
            color: $color-dark;
            text-decoration: none;
            display: inline-block;
            transition: all .3s;
            box-shadow: none;
            -webkit-tap-highlight-color: transparent;

            &:visited {
                color: $color-dark;
            }

            &:hover {
                color: $color-accent;
                box-shadow: 0 4px 0 0 $color-accent;
            }

            &:active {
                color: $color-dark;
            }

            &.router-link-exact-active {
                color: $color-accent;
                box-shadow: 0 4px 0 0 $color-accent;
                pointer-events: none;
            }

        }

        &.minimized {
            height: 38px;
        }
    }

    #nav.nav-menu-active {
        height: 70px;
    }

    #brand {
        font-family: 'disposabledroid_bbbold';
        font-size: 40px;
        background-color: $color-primary;
        color: #ffffff;
        padding: 10px;
        box-shadow: 0.22rem 0.22rem 0 $color-dark;
        transform: skew(0deg, -5deg) scaleX(0.9);
        user-select: none;
margin: 0px 0px 30px;
    }

    .moonstone-blue {
        color: $color-light
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

    /*Inria Sans*/

    @font-face {
        font-family: 'inria_sansbold';
        src: url('./assets/fonts/inria_sans/inriasans-bold-webfont.woff2') format('woff2'),
        url('./assets/fonts/inria_sans/inriasans-bold-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;

    }

    @font-face {
        font-family: 'inria_sansbold_italic';
        src: url('./assets/fonts/inria_sans/inriasans-bolditalic-webfont.woff2') format('woff2'),
        url('./assets/fonts/inria_sans/inriasans-bolditalic-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;

    }

    @font-face {
        font-family: 'inria_sansitalic';
        src: url('./assets/fonts/inria_sans/inriasans-italic-webfont.woff2') format('woff2'),
        url('./assets/fonts/inria_sans/inriasans-italic-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;

    }

    @font-face {
        font-family: 'inria_sansregular';
        src: url('./assets/fonts/inria_sans/inriasans-regular-webfont.woff2') format('woff2'),
        url('./assets/fonts/inria_sans/inriasans-regular-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;

    }

    @media screen and (max-width: 900px) {
        #app {
            padding: 0;
            grid-template-rows: 200px;
            grid-template-columns: 1fr;
            grid-template-areas: "nav"
        "content";
        }

        .nav-container {
            grid-area: nav;
            display: flex;
            flex-direction: row;

            align-items: flex-start;
            justify-content: space-around;
            padding: 36px 31px 45px 0px;
        }
        nav {
            flex-direction: column;
            align-items: flex-start;
            a {
                user-select: none;
                margin: 8px 0px;
                font-family: 'inria_sansbold';
                font-weight: bold;
                font-size: 20px;}
        }

        #brand {
            align-self: center;
            margin: 0;
        }
    }
</style>
