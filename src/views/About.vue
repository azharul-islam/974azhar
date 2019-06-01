<template>
    <div class="about">
        <span class="container header">About Me</span>
        <div class="container talk-bubble tri-right left-top">
            <p>Hi! 👋🏻 I'm a full-stack software developer based in Qatar. I am currently
                specialised in Mobile and Web apps.
                <br><br>
                If you want to get in touch, write me an email on azhar.i@outlook.com.</p>

            <img src="../assets/azhar.jpg" height="100"/>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    $color-dark: #1c4e6c;

    .container {
        padding: 18px;
        margin: 10px 28px;


    }

    .talk-bubble {
        margin:  0 40px 40px 40px;
        display: inline-block;
        position: relative;
        width: 200px;
        height: auto;
    }

    .about {
        margin: 200px 0 0 0;
        position: relative;
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
