<script setup>
import FontFaceObserver from "fontfaceobserver";
import { ref, onMounted, reactive } from 'vue';

// 字体加载完成后再渲染页面
const font1 = new FontFaceObserver("Playfair Display Regular");
const font2 = new FontFaceObserver("Playfair Display Italic");
const loaded = ref(false);
Promise.all([font1.load(), font2.load()]).then(function () {
    loaded.value = true;
});

// 鼠标移动更改标题字重
onMounted(() => { window.addEventListener('mousemove', handleMouseMove) })
const handleMouseMove = e => {
    changeWeight(e.clientX, e.clientY);
}
const changeWeight = (x, y) => {
    let weight = x * 0.6;
    let opsz = 100 + y * 2;
    // 限制opsz最小值以避免字形发生改变
    const minOpsz = 411;
    opsz <= minOpsz ? opsz = minOpsz : opsz = opsz;
    document.querySelector('#title').style.fontVariationSettings = `'wght' ${weight},'opsz' ${opsz}`;
}
</script>

<template>
    <div class="container" v-if="loaded">
        <div class="box">
            <h1 id="title">Chris Jia</h1>
            <div class="subtitle">is a dreamer and a designer</div>
            <div class="main">
                You can find me on
                <a class="link" href="https://weibo.com/u/6506391030">weibo</a> and
                <a class="link" href="https://www.instagram.com/jiia.cc/">instagram</a>,
                and see my works on
                <a class="link" href="https://dribbble.com/chrisjia">Dribbble</a>.
                <br />Know me more at my
                <a class="link" href="https://blog.choki.xyz">
                    <span>blog</span>
                </a>. Contact me via
                <a class="link" href="mailto:chokij@outlook.com">email</a>.
            </div>
        </div>
    </div>
</template>

<style>
h1 {
    font-family: Playfair Display Regular;
    font-style: normal;
    font-size: 96px;
    line-height: 128px;
    text-align: center;
    color: #2c3e50;
    margin-bottom: 0px;
    margin-top: 0px;
    -webkit-animation: 2s ease h1anime;
    animation: 2s ease h1anime;
    font-variation-settings: 'opsz' 1000, 'wght' 900;
}

@keyframes h1anime {
    from {
        font-variation-settings: "wght" 100, 'opsz' 100;
    }

    to {
        font-variation-settings: "wght" 900, 'opsz' 1000;
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
    font-variation-settings: 'opsz' 1000;
}

.link {
    font-family: Playfair Display Italic;
    font-style: normal;
    font-weight: 500;
    font-size: 26px;
    line-height: 36px;
}

.container {
    display: block;
    width: 100%;
    height: 100%;
}

.box {
    position: relative;
    top: 30%;
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

a {
    color: #2c3e50;
    transition: all 0.3s ease;
}

a:hover {
    background-color: #2c3e50;
    color: #ffffff;
}
</style>
