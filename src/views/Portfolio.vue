<template>
    <div class="about">

        <h2 class="accordion-header container collapser" @click="toggleCollapsible(0)" :class="{expanded: toggles[0]}">Mobile Apps <span
                class="chevron bottom"
                :class="{toggled: toggles[0]}"></span>
        </h2>
        <div ref="a" class="collapsible" :class="{expanded: toggles[0]}" :style="{maxHeight: heights[0]}">
            <h3>Alaqat</h3>
            <p>Android app developed for a media company that provides services like promotions, video productions &
                social media influencers coverage.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/alaqat/1.png" alt="">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/alaqat/2.png" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>Droobi</h3>
            <p>An app designed & developed by me during my full-time position at Droobi Health. It was an mHealth
                mobile app for Diabetes Management.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/droobi/1.png" alt="">
                </swiper-slide>

                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>Passwordless</h3>
            <p>An app designed & developed by me for Senior Design
                Project, that allowed logging into any website just
                like Whatsapp Web, taking into account multiple
                factors like location, time, etc.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/passwordless/1.png" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>Smart Transportation</h3>
            <p>An app designed & developed by me that allowed a
                bus driver to track his/her location and student to
                monitor locations of all buses, in realtime.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/smarttransportation/1.jpg" alt="">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/smarttransportation/2.jpg" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>Discs Watchface</h3>
            <p>Watchface designed and developed by me as a side
                project. It was then deployed to Play Store for
                Android wear compatible smartwatches. Also, the
                promos here were photographed, edited and/or
                designed by me.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/discs/1.jpg" alt="">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/discs/2.jpg" alt="">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/discs/3.jpg" alt="">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/discs/4.jpg" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
        </div>

        <h2 class="accordion-header container collapser" @click="toggleCollapsible(1)" :class="{expanded: toggles[1]}">Web Apps/Sites
            <span
                    class="chevron bottom"
                    :class="{toggled: toggles[1]}"></span>
        </h2>
        <div ref="b" class="collapsible" :class="{expanded: toggles[1]}" :style="{maxHeight: heights[1]}">
            <h3>titanium.com.bd</h3>
            <p>Landing page for an LED lighting manufacturer in Bangladesh. Designed and developed by me.</p>
            <p><b>Technology:</b> Vue.JS, CSS Grid, Flexbox, Netlify hosting and CDN with Continuous Integration,
                Firestore</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/titanium/2.jpg" alt=""
                                                       style=" background-color: white; max-height:  420px;">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/titanium/3.jpg" alt=""
                                                       style="background-color: white; max-height: 420px;">
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/titanium/4.jpg" alt=""
                                                       style=" background-color: white; max-height:  420px;">
                </swiper-slide>

                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>

            <hr>
            <h3>qqqsite.com</h3>
            <p>Website designed and developed for a comedian/social media influencer. </p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/qqq/1.jpg" alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/qqq/2.jpg" alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/qqq/3.jpg" alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/qqq/4.jpg" alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/qqq/5.jpg" alt=""
                >
                </swiper-slide>

                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>droobihealth.com</h3>
            <p>Landing page for Droobi Health.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/droobiweb/1.jpg" alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/droobiweb/2.jpg" alt=""
                >
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>Intervention Messages Algorithm Simulator</h3>
            <p>At Droobi Health W.L.L., while we were working on an algorithm for sending out notification, intervention
                and reminder messages, I had developed a simulator to help better understand the flow and allow easier
                explanation to stakeholders during presentations.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/web_droobialgorithmsimulator/1.jpg"
                                                       alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/web_droobialgorithmsimulator/2.jpg"
                                                       alt=""
                >
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>Card Printer</h3>
            <p>A reactive web app developed for printing serial numbers on pre-printed warranty cards. </p>

            <p>Tech Stack
                HTML, CSS, Flexbox, Javascript, Vue.JS</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/web_warrantyprinter/1.jpg"
                                                       alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/web_warrantyprinter/2.jpg"
                                                       alt=""
                >
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
            <hr>
            <h3>ERP</h3>
            <p>A web-based ERP customized and implemented.</p>

            <p>Tech Stack
                HTML, CSS, Flexbox, Javascript, Vue.JS</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/erp/1.jpg"
                                                       alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/erp/2.jpg"
                                                       alt=""
                >
                </swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/erp/3.jpg"
                                                       alt=""
                >
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
        </div>


        <h2 class="accordion-header container collapser" @click="toggleCollapsible(2)" :class="{expanded: toggles[2]}">Photography <span
                class="chevron bottom"
                :class="{toggled: toggles[2]}"></span>
        </h2>
        <div ref="c" class="collapsible" :class="{expanded: toggles[2]}" :style="{maxHeight: heights[2]}">
            <h3>Portraits</h3>
            <hr>
            <h3>Landscapes</h3>
            <hr>
            <h3>Food</h3>
        </div>
        <h2 class="accordion-header container collapser" @click="toggleCollapsible(3)" :class="{expanded: toggles[3]}">Logo Design <span
                class="chevron bottom"
                :class="{toggled: toggles[3]}"></span>
        </h2>
        <div ref="d" class="collapsible" :class="{expanded: toggles[3]}" :style="{maxHeight: heights[3]}">

            <h3>Logo Design</h3>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/logodesign/1.png" alt=""></swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>

            </swiper>

        </div>
        <h2 class="accordion-header container collapser" @click="toggleCollapsible(4)" :class="{expanded: toggles[4]}">3D Modelling <span
                class="chevron bottom"
                :class="{toggled: toggles[4]}"></span>
        </h2>
        <div ref="e" class="collapsible" :class="{expanded: toggles[4]}" :style="{maxHeight: heights[4]}">
            <h3>3D Modelling</h3>

            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/3d/1.jpg" alt=""></swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>

            </swiper>

        </div>
        <h2 class="accordion-header container collapser" @click="toggleCollapsible(5)" :class="{expanded: toggles[5]}">Brochure Design
            <span
                    class="chevron bottom"
                    :class="{toggled: toggles[5]}"></span>
        </h2>
        <div ref="f" class="collapsible" :class="{expanded: toggles[5]}" :style="{maxHeight: heights[5]}">
            <h3>Tri-Folding Brochure</h3>
            <p>A tri-folding brochure designed for Droobi Diabetes management app in Adobe Indesign</p>

            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/brochure/1.jpg" alt=""></swiper-slide>
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/brochure/2.jpg" alt=""></swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>

            </swiper>

        </div>
        <h2 class="accordion-header container collapser" @click="toggleCollapsible(6)" :class="{expanded: toggles[6]}">Game Design <span
                class="chevron bottom"
                :class="{toggled: toggles[6]}"></span>
        </h2>
        <div ref="g" class="collapsible" :class="{expanded: toggles[6]}" :style="{maxHeight: heights[6]}">
            <h3>Game Level Design</h3>
            <p>Designed and developed this game level using Unity 3D & Blender.

                Challenges included,
                -Navigating the boat among the rocks. Turning too much however would cause the boat to topple
                -Reaching destination on time.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/game/1.jpg" alt=""></swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>

            </swiper>

        </div>
        <h2 class="accordion-header container collapser" @click="toggleCollapsible(7)" :class="{expanded: toggles[7]}">Miscellany
            <span
                    class="chevron bottom"
                    :class="{toggled: toggles[7]}"></span>
        </h2>
        <div ref="h" class="collapsible" :class="{expanded: toggles[7]}" :style="{maxHeight: heights[7]}">
            <h3>Print Formats Design and Development</h3>
            <p>I had to take the old quotation layout and modernize it. I tried to present important information clearly
                and at the same time minimize or hide distracting information. I aimed to create a minimal design that
                matched the branding of the company. It was important for a quotation to look it’s best as it was the
                very first point of contact with a lead.

                I also made the design bolder as I believed it would project confidence and lend credibility to the
                company.
                <br>
                <strong>Technology leveraged:</strong> HTML, CSS, Jinja Templating
            </p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/printformat/1.png" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>

            </swiper>
            <hr>
            <h3>Business Cards Design</h3>
            <p>Designed by me using Adobe Illustrator for Droobi Health W.L.L.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/businesscard/1.jpg" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>

            </swiper>
            <hr>
            <h3>Map Art</h3>
            <p>I created this map art using snazzymaps.com and Adobe Photoshop, for my city. Then, I printed and framed them in Ikea frames and sold them.</p>
            <swiper :options="swiperOption" ref="mySwiper">
                <swiper-slide class="swiper-item"><img src="../assets/portfolio/mapart/1.jpg" alt="">
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
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
                    spaceBetween: 10,


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
                            this.$set(this.heights, value, 'none')
                        }
                        break;
                    case 1:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, 'none')
                        }
                        break;
                    case 2:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, 'none')
                        }
                        break;
                    case 3:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, 'none')
                        }
                        break;
                    case 4:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, 'none')
                        }
                        break;
                    case 5:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, 'none')
                        }
                        break;
                    case 6:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value, 'none')
                        }
                        break;
                    case 7:
                        if (this.toggles[value]) {
                            this.$set(this.heights, value, '0');
                        } else {
                            this.$set(this.heights, value,'none')
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
        margin: 10px 0 20px 0;

        display: grid;
        grid-template-columns: minmax(100px, 900px);
        justify-content: center;
    }

    img {
        text-align: center;
        max-width: 90%;
        margin-bottom: 35px;
        margin-left: auto;
        margin-right: auto;
        max-height: 480px;
    }

    p {
        /*font-family: 'Roboto Slab', serif;*/
        /*font-family: 'disposabledroid_bbregular', serif;*/
        /*font-size: 17px;*/
        /*line-height: 1.4;*/

        font-family: 'Noto Sans HK', sans-serif;
        font-weight: 500;
        font-size: 14px;
        line-height: 1.8;
        margin-block-start: 0em;
        margin-block-end: 0em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
        padding: 0px 16px 14px;
    }


    h1, h2, h3 {
        margin-block-start: 0em;
        margin-block-end: 0em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
        padding: 18px 16px;
    }

    .accordion-header {
        font-size: 20px;
    }

    hr {
        margin-block-start: 0em;
        margin-block-end: 0em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
        background-color: transparent;
    }


    .collapser {
        cursor: pointer;
        -webkit-tap-highlight-color: transparent;
        transition: all 0.15s;
        position: relative;
        margin: 0px 16px 0px 16px;
    }

    .collapsible {
        user-select: none;
        background-color: #FFFFFF;
        max-height: 0;
        overflow: hidden;
        margin: 0px 16px 4px 16px;

        &.expanded {
        }
    }

    .chevron::before {
        margin: 5px 8px 0 0;
        float: right;
        border-style: solid;
        border-width: 2px 2px 0 0;
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


    .swiper-item {
        object-fit: cover;
        max-width: 400px;

    }
</style>
