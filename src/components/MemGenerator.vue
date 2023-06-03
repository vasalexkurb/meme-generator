
<script>
export default {
    data() {
        return {
            topText: ``,
            bottomText: ``,
        
            topTextPosX: 0,
            topTextPosY: 0,

            bottomTextPosX: 0,
            bottomTextPosY: 0,

            topFontSize: 30,
            bottomFontSize: 30,

            imageUrl: `https://www.meme-arsenal.com/memes/048348d157ac1073c62e7a3773555349.jpg`
        }
    }
}

</script>


<template>
    <div class="mem-gen">
        <div class="meme">
            <p :style="{
                left: topTextPosX + `px`,
                top: topTextPosY + `px`,
                fontSize: topFontSize + `px`
            }" class="top-text">
                {{ topText }}
            </p>
            <p :style="{
                left: bottomTextPosX + `px`,
                top: bottomTextPosY + `px`,
                fontSize: bottomFontSize + `px`
            }" class="bottom-text">
                {{ bottomText }}
            </p>
            <img :src="imageUrl">
        </div>

        <hr>

        <div class="input-group mb-3">
            <span class="input-group-text">Верхняя надпись</span>
            <textarea v-model="topText" class="form-control"></textarea>
        </div>
        <div class="input-group mb-3">
            <span class="input-group-text">По горизонтали:</span>
            <input v-model="topTextPosX" type="range" class="form-control" min="-300" max="300">
        </div>

        <div class="input-group mb-3">
            <span class="input-group-text">По вертикали:</span>
            <input v-model="topTextPosY" type="range" class="form-control" min="-300" max="300">
        </div>
        
        <div class="input-group mb-3">
            <span class="input-group-text">Размер шрифта:</span>
            <input v-model="topFontSize" type="range" class="form-control" min="20" max="60">
        </div>

        <div class="text-muted fs-5">
            Текущий размер: {{ topFontSize }} пикселей
        </div>

        <hr style="width: 100%">
        <div class="input-group mb-3">
            <span class="input-group-text">Нижняя надпись</span>
            <textarea v-model="bottomText" class="form-control"></textarea>
        </div>
        
        <div class="input-group mb-3">
            <span class="input-group-text">По горизонтали:</span>
            <input v-model="bottomTextPosX" type="range" class="form-control" min="-300" max="300">
        </div>

        <div class="input-group mb-3">
            <span class="input-group-text">По вертикали:</span>
            <input v-model="bottomTextPosY" type="range" class="form-control" min="-300" max="400">
        </div>

        <div class="input-group mb-3">
            <span class="input-group-text">Размер шрифта:</span>
            <input v-model="bottomFontSize" type="range" class="form-control" min="20" max="60">
        </div>

        <div class="text-muted fs-5 mb-3">
            Текущий размер: {{ bottomFontSize }} пикселей
        </div>

        <div class="input-group mb-3">
            <span class="input-group-text">Изображение</span>
            <textarea v-model="imageUrl" class="form-control"></textarea>
        </div>
    </div>
</template>

<style>
.mem-gen img {
    max-width: 500px;
    width: 100%;
    height: auto;
}

.mem-gen .meme {
    position: relative;
    text-align: center;
}

.mem-gen span {
    width: 150px;
}

.top-text {
    position: absolute;
    left: 0;
}

.bottom-text {
    position: absolute;
    left: 0;
}

.top-text,
.bottom-text {
    width: 100%;
    text-align: center;
    color: #ffffff;
    font-family: 'Arial', sans-serif;
    font-weight: 700;
    margin: 0;
    text-shadow:
        0 -2px 0 #000000,
        0 2px 0 #000000,
        -2px -0 0 #000000,
        2px -0 0 #000000,
        -2px 0 0 #000000,
        2px 0 0 #000000,
        -1px -2px 0 #000000,
        1px -2px 0 #000000,
        -1px 2px 0 #000000,
        1px 2px 0 #000000,
        -2px -1px 0 #000000,
        2px -1px 0 #000000,
        -2px 1px 0 #000000,
        2px 1px 0 #000000,
        -2px -2px 0 #000000,
        2px -2px 0 #000000,
        -2px 2px 0 #000000,
        2px 2px 0 #000000;
}

.top-text {
    top: 20px;
}

.bottom-text {
    bottom: 20px;
}

hr {
    margin: 40px auto;
    width: 50%;
    height: 8px;
    background-color: #41b883;
    border: 0;
    border-top: 3px solid #35495e;
}
</style>