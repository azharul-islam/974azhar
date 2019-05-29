<template>
    <div class="about">
        <div class="container">
            <div class="collapser" @click="">
                <h2>Mobile Apps <span class="chevron bottom"></span></h2>
                <hr>
            </div>

            <div class="collapsible">
                <h3>Alaqat</h3>
                <hr>
                <h3>Droobi</h3>
                <hr>
                <h3>Passwordless</h3>
                <hr>
                <h3>Smart Transportation</h3>
                <hr>
                <h3>Discs Watchface</h3>
            </div>
        </div>
        <div class="container">
            <h2>Web Apps/Sites <span class="chevron bottom"></span></h2>
        </div>
        <div class="container">
            <h2>Photography <span class="chevron bottom"></span></h2>
        </div>
        <div class="container">
            <h2>Logo Design <span class="chevron bottom"></span></h2>
        </div>
        <div class="container">
            <h2>3D Modelling <span class="chevron bottom"></span></h2>
        </div>
        <div class="container">
            <h2>Brochure Design <span class="chevron bottom"></span></h2>
        </div>
        <div class="container">
            <h2>Game Design <span class="chevron bottom"></span></h2>
        </div>
        <div class="container">
            <h2>Miscellaneous <span class="chevron bottom"></span></h2>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'Portfolio',
        props: {},
        data: function () {
            return {
                toggles: [false, false, false, false, false, false, false, false],
            }
        },
        methods: {
            toggleCollapsible(value) {
                return `${value.toFixed(0)}`.replace(/(\d)(?=(\d{3})+(?!\d))/g, '$1,');
            },

        }

    }
</script>

<style lang="scss" scoped>
    $color-dark: #1c4e6c;


    .about {
        margin: 135px 0 0 0;
    }

    p {
        font-family: 'disposabledroid_bbregular', sans-serif;
        font-size: 18px;
    }

    hr {
        border-top: 1px solid $color-dark;
        background-color: transparent;
    }

    h1, h2, h3 {
        margin-block-start: 0em;
        margin-block-end: 0em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
        padding: 18px;
    }

    hr {
        margin-block-start: 0em;
        margin-block-end: 0em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
    }

    img {
        border: 3px solid $color-dark;
        box-shadow: 0.2rem 0.2rem 0 $color-dark;
        border-radius: 50%;
    }

    .collapser {

    }

    .chevron::before {
        margin: 0px 10px;
        float: right;
        border-style: solid;
        border-width: 3px 3px 0 0;
        content: '';
        display: inline-block;
        height: 0.45em;
        transform: rotate(-45deg);
        width: 0.45em;
    }

    .chevron.right:before {
        left: 0;
        transform: rotate(45deg);
    }

    .chevron.bottom:before {
        top: 0;
        transform: rotate(135deg);
    }

    .chevron.left:before {
        left: 0.25em;
        transform: rotate(-135deg);
    }

</style>
