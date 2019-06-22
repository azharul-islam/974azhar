<template>
    <div class="about">
        <div class="container talk-bubble tri-right left-top">
<!--            <span class="container header">About Me</span>-->
            <p>Hi! 👋🏻 My name is Azharul Islam. I'm a professional full-stack Software Developer since 2016, based in Qatar.
                specialised in Mobile and Web apps.</p>
            <img src="../assets/azhar.jpg" height="100"/>
        </div>

        <div class="container talk-bubble">
            To get in touch you can <a href="mailto:azhar.i@outlook.com?Subject=Hello" target="_top">mail</a> me on azhar.i@outlook.com or <a href="https://wa.me/97433338469" title="Text on WhatsApp">whatsapp</a> me on +974 3333 8469.

        </div>
    </div>
</template>

<style lang="scss" scoped>
    $color-dark: #1c4e6c;

    .container {
        padding: 14px;
        margin: 10px 28px;
    }

    .talk-bubble {
        margin:  0 90px 10px 35px;
        display: inline-block;
        position: relative;
        height: auto;

        font-size: 17px;
        line-height: 1.7;

        a {
            box-shadow: 0 2px 0 0 currentColor;

        }

    }

    .about {
        grid-area: content;
        font-family: 'inria_sansregular', sans-serif;

        margin: 10px 0 0 0;
        position: relative;
        display: grid;
        grid-template-columns: minmax(200px, 700px);
        justify-content: center;
    }

    p {

        margin-block-start: 0em;
        margin-block-end: 0.8em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
    }

    h1 {
        margin-block-start: 0em;
        margin-block-end: 0em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
    }

    .header {
        font-family: 'disposabledroid_bbbold', sans-serif;
        font-size: 20px;
        transform: rotate(-9deg);
        box-shadow: 0.22rem 0.22rem 0 $color-dark;
        position: absolute;
        top: -90px;
        left: -20px;
    }

    img {
        border-radius: 50%;
        border: 2px solid #efefef;
    }

    .tri-right.left-top:before {
        content: ' ';
        position: absolute;
        width: 0;
        height: 0;
        left: -25px;
        right: auto;
        top: -2px;
        bottom: auto;
        border: 23px solid;
        border-color: transparent transparent transparent transparent;
    }

    .tri-right.left-top:after {
        content: ' ';
        position: absolute;
        width: 0;
        height: 0;
        left: -20px;
        right: auto;
        top: 0px;
        bottom: auto;
        border: 22px solid;
        border-color: white transparent transparent transparent;
    }

    @media screen and (min-width: 992px) {
        .talk-bubble {
            margin:  0 90px 10px 35px;
            display: inline-block;
            position: relative;
            height: auto;
            font-size: 21px;
            line-height: 1.7;

            a {
                box-shadow: 0 2px 0 0 currentColor;
            }

        }

    }

</style>
