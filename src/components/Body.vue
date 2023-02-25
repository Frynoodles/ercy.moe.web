<script setup lang="ts">
</script>
<template>
    <div class="main-content-box">
        <div class="main-content">
            <div class="column-box" id="left-box">
                <div class="white-box"></div>
                <div class="white-box"></div>
            </div>
            <div class="column-box" id="right-box">
                <div class="white-box"></div>
                <div class="white-box"></div>
                <img src="https://raw.githubusercontent.com/Frynoodles/frynoodles/main/%E9%A9%AC%E6%81%A9%E5%88%97%E6%96%AF%E6%AF%9B.jpg" alt="">
            </div>
        </div>
    </div>
</template>

<style scoped lang="less">
.main-content-box {
    padding: 0%;
    margin: 0%;
    height: 2000px;
    width: 100%;
    display: flex;
    justify-content: center;

    .main-content {
        height: 100%;
        width: 900px;
        display: flex;
        justify-content: center;
        margin: 20px;
        border-radius: 20px;
        background-color: cadetblue;

        .column-box {
            display: flex;
            flex-direction: column;
            justify-content: start;
            align-items: center;
            margin: 0%;
            padding: 0%;

            .white-box {
                width: 400px;
                height: 400px;
                background-color: aliceblue;
                border-radius: 20px;
                margin: 20px;
            }
        }

    }

}
</style>