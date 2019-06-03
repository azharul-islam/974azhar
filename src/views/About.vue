<template>
    <div class="about">
        <div class="container talk-bubble tri-right left-top">
<!--            <span class="container header">About Me</span>-->
            <p>Hi! 👋🏻 My name is Azharul Islam. I'm a full-stack Software Developer based in Qatar,
                specialised in Mobile and Web apps.
                <br><br>
                If you want to get in touch, shoot me an <a href="mailto:azhar.i@outlook.com?Subject=Hello" target="_top">email</a> on azhar.i@outlook.com or <a href="https://web.whatsapp.com/send?phone=97433338469" title="Text on WhatsApp">whatsapp</a> me on +974 3333 8469.</p>

            <img src="../assets/azhar.jpg" height="100"/>
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
        margin:  0 90px 40px 35px;
        display: inline-block;
        position: relative;
        /*width: 250px;*/
        height: auto;
    }

    .about {
        margin: 10px 0 0 0;
        position: relative;
        display: grid;
        grid-template-columns: minmax(200px, 500px);
        justify-content: center;
    }

    p {
        font-family: 'disposabledroid_bbregular', sans-serif;
        font-size: 18px;
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
        border-color: $color-dark transparent transparent transparent;
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


</style>
