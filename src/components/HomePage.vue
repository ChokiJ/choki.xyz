<script setup>
</script>

<template>
    <div class="box">
        <h1 title>Chris Jia</h1>
        <a class="subtitle">is a student and a designer</a>
        <div class="main">
            You can find me on
            <a class="link" href="https://weibo.com/u/6506391030">weibo</a> and
            <a class="link" href="https://www.instagram.com/choki.redfield/">instagram</a>,
            and see my works on
            <a
                class="link"
                href="https://www.behance.net/Chokijf4b3"
            >Behance</a>.
            <br />Know me more at my
            <a class="link" href="https://blog.choki.xyz">
                <span>blog</span>
            </a>. Contact me via
            <a class="link" href="mailto:chokij@outlook.com">email</a>.
        </div>
    </div>
</template>

<style>
h1 {
    font-family: Playfair Display Regular;
    font-style: normal;
    font-weight: 900;
    font-size: 96px;
    line-height: 128px;
    text-align: center;
    color: #2c3e50;
    margin-bottom: 0px;
    margin-top: 0px;
    -webkit-animation: 2s ease h1anime;
    animation: 2s ease h1anime;
}

@-webkit-keyframes h1anime {
    from {
        font-variation-settings: "wght" 400;
    }
    to {
        font-variation-settings: "wght" 900;
    }
}
@keyframes h1anime {
    from {
        font-variation-settings: "wght" 400;
    }
    to {
        font-variation-settings: "wght" 900;
    }
}

.subtitle {
    font-family: Playfair Display Italic;
    font-style: normal;
    font-weight: normal;
    font-size: 26px;
    line-height: 36px;
    text-align: center;
    color: #2c3e50;
    display: block;
}

.main {
    font-family: Playfair Display Regular;
    font-style: nomral;
    font-weight: normal;
    font-size: 26px;
    line-height: 36px;
    color: #2c3e50;
    display: block;
    text-align: center;
    padding-top: 1rem;
}
.link {
    font-family: Playfair Display Italic;
    font-style: normal;
    font-weight: 500;
    font-size: 26px;
    line-height: 36px;
    color: #2c3e50;
}
.box {
    display: block;
    width: 70vw;
}

body {
    width: 100vw;
    height: 100vh;
    margin: 0;
    padding: 0;
    display: flex;
    background-color: rgb(250, 246, 243);
    justify-content: center;
    align-items: center;
}
</style>
