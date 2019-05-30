<template>
    <div class="about">

        <h2 class="container collapser" @click="toggleCollapsible(0)" :class="{expanded: toggles[0]}">Mobile Apps <span
                class="chevron bottom"
                :class="{toggled: toggles[0]}"></span>
        </h2>
        <div ref="a" class="collapsible" :class="{collapsed: toggles[0]}" :style="{maxHeight: heights[0]}">
            <h3>Alaqat</h3>
            <p>Android app developed for a media company that provides services like promotions, video productions &
                social media influencers coverage.</p>
            <swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/alaqat/1.jpg" alt="">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/alaqat/2.jpg" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>Droobi</h3>
            <p>An app designed & developed by me during my full-
                time position at Droobi Health. It was an mHealth
                mobile app for Diabetes Management.</p>
            <swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/alaqat/1.jpg" alt="">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/alaqat/2.jpg" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>Passwordless</h3>
            <p>An app designed & developed by me for Senior Design
                Project, that allowed logging into any website just
                like Whatsapp Web, taking into account multiple
                factors like location, time, etc.</p>
            <hr>
            <h3>Smart Transportation</h3>
            <p>An app designed & developed by me that allowed a
                bus driver to track his/her location and student to
                monitor locations of all buses, in realtime.</p>
            <hr>
            <h3>Discs Watchface</h3>
            <p>Watchface designed and developed by me as a side
                project. It was then deployed to Play Store for
                Android wear compatible smartwatches. Also, the
                promos here were photographed, edited and/or
                designed by me.</p>
        </div>

        <h2 class="container collapser" @click="toggleCollapsible(1)" :class="{expanded: toggles[1]}">Web Apps/Sites <span
                class="chevron bottom"
                :class="{toggled: toggles[1]}"></span>
        </h2>
        <div ref="b" class="collapsible" :class="{collapsed: toggles[1]}" :style="{maxHeight: heights[1]}">
            <h3>qqqsite.com</h3>
            <hr>
            <h3>droobihealth.com</h3>
            <hr>
            <h3>dta.qa</h3>
            <hr>
            <h3>Intervention Messages Algorithm Simulator</h3>
            <hr>
            <h3>Card Printer</h3>
        </div>


        <h2 class="container collapser" @click="toggleCollapsible(2)" :class="{expanded: toggles[2]}">Photography <span
                class="chevron bottom"
                :class="{toggled: toggles[2]}"></span>
        </h2>
        <div ref="c" class="collapsible" :class="{collapsed: toggles[2]}"  :style="{maxHeight: heights[2]}">
            <h3>Portraits</h3>
            <hr>
            <h3>Landscapes</h3>
            <hr>
            <h3>Food</h3>
        </div>
        <h2 class="container collapser" @click="toggleCollapsible(3)" :class="{expanded: toggles[3]}">Logo Design <span
                class="chevron bottom"
                :class="{toggled: toggles[3]}"></span>
        </h2>
        <div ref="d" class="collapsible" :class="{collapsed: toggles[3]}"  :style="{maxHeight: heights[3]}">
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
        <h2 class="container collapser" @click="toggleCollapsible(4)" :class="{expanded: toggles[4]}">3D Modelling <span
                class="chevron bottom"
                :class="{toggled: toggles[4]}"></span>
        </h2>
        <div ref="e" class="collapsible" :class="{collapsed: toggles[4]}"  :style="{maxHeight: heights[4]}">
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
        <h2 class="container collapser" @click="toggleCollapsible(5)" :class="{expanded: toggles[5]}">Brochure Design <span
                class="chevron bottom"
                :class="{toggled: toggles[5]}"></span>
        </h2>
        <div ref="f" class="collapsible" :class="{collapsed: toggles[5]}"  :style="{maxHeight: heights[5]}">
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
        <h2 class="container collapser" @click="toggleCollapsible(6)" :class="{expanded: toggles[6]}">Game Design <span
                class="chevron bottom"
                :class="{toggled: toggles[6]}"></span>
        </h2>
        <div ref="g" class="collapsible" :class="{collapsed: toggles[6]}"  :style="{maxHeight: heights[6]}">
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
        <h2 class="container collapser" @click="toggleCollapsible(7)" :class="{expanded: toggles[7]}">Miscellaneous <span
                class="chevron bottom"
                :class="{toggled: toggles[7]}"></span>
        </h2>
        <div ref="h" class="collapsible" :class="{collapsed: toggles[7]}"  :style="{maxHeight: heights[7]}">
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
</template>

<script>

    export default {
        name: 'Portfolio',
        props: {},
        data: function () {
            return {
                toggles: [false, false, false, false, false, false, false, false],
                heights: ['0', '0', '0', '0', '0', '0', '0', '0'],
                swiperOption: {
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true
                    },
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev',
                    },
                    slidesPerView: 'auto',
                    centeredSlides: true,

                }
            }
        },
        methods: {
            toggleCollapsible(value) {


                switch (value) {
                    case 0:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, this.$refs.a.scrollHeight + 'px')
                        }
                        break;
                    case 1:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, this.$refs.b.scrollHeight + 'px')
                        }
                        break;
                    case 2:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, this.$refs.c.scrollHeight + 'px')
                        }
                        break;
                    case 3:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, this.$refs.d.scrollHeight + 'px')
                        }
                        break;
                    case 4:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, this.$refs.e.scrollHeight + 'px')
                        }
                        break;
                    case 5:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, this.$refs.f.scrollHeight + 'px')
                        }
                        break;
                    case 6:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, this.$refs.g.scrollHeight + 'px')
                        }
                        break;
                    case 7:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, this.$refs.h.scrollHeight + 'px')
                        }
                        break;
                    default:
                        break;
                }


                this.$set(this.toggles, value, !this.toggles[value])
            },

        }

    }
</script>

<style lang="scss" scoped>
    $color-dark: #1c4e6c;


    .about {
        margin: 125px 0 0 0;
    }

    img {
        /*border: none;*/
        max-width: 90%;
        margin-bottom: 35px;
        margin-left: 5%;
        /*<!--box-shadow: 0.15rem 0.15rem 0 $color-dark;-->*/

        border: 1px solid $color-dark;
    }

    p {
        font-family: 'disposabledroid_bbregular', sans-serif;
        font-size: 18px;
        margin-block-start: 0em;
        margin-block-end: 0em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;

        padding: 0px 18px 18px;
    }

    hr {
        border-top: 1px solid $color-dark;
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


    .collapser {
        cursor: pointer;
        -webkit-tap-highlight-color: transparent;
        transition: all 0.15s;
        position: relative;
        margin: 0px 10px 0px 10px;
    }

    .collapser.expanded {

    }

    .collapsible {
        user-select: none;



        background-color: #F4F4F4;
        max-height: 0;
        border-top: none;
        border-bottom: none;
        overflow: hidden;
        transition: max-height 0.25s ease-in-out;
        margin: 0px 10px 10px 10px;
        border-right: 3px solid $color-dark;
        border-left: 3px solid $color-dark;

        &.collapsed {

            border-bottom: 3px solid $color-dark;
        }
    }

    .chevron::before {
        margin: 0 8px 0 0;
        float: right;
        border-style: solid;
        border-width: 3px 3px 0 0;
        content: '';
        display: inline-block;
        height: 0.45em;
        transform: rotate(-45deg);
        width: 0.45em;
        left: 0.15em;
        position: relative;
        top: 0.15em;
        transition: all 0.2s;
        vertical-align: middle;
    }


    .chevron.bottom:before {
        top: 0;
        transform: rotate(135deg);
    }

    .chevron.toggled:before {
        transform: rotate(-45deg);
        top: 0.25em;
    }

</style>
