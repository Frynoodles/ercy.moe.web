<template>
    <div>
        <div class="header">
            <div class="header-content">

                <div class="left-content">
                    <div class="logo item-wrapper  content-box">
                        <a href="http://ercy.moe/">
                            <img src="../icons/logo_beta_v0.3.png" alt="HideRua:没吃饭可以上厕所吗？" id="header-logo">
                        </a>
                    </div>
                </div>

                <div class="center-content">
                    <div class="menu-bar item-wrapper  content-box">
                        <div class="menu-item">
                            <a href="">首 页</a>
                        </div>
                        <div class="menu-item dividing-line">
                        </div>
                        <div class="menu-item">
                            <a href="">学 习 笔 记</a>
                        </div>
                        <div class="menu-item dividing-line">
                        </div>
                        <div class="menu-item">
                            <a href="">收 藏 夹</a>
                        </div>
                    </div>
                </div>

                <div class="right-content">
                    <div class="media-links item-wrapper content-box">
                        <div class="face">
                            <img src="../icons/face.jpg" class="media-icon" id="face-icon">
                        </div>
                        <div class="media-link">
                            <a href="https://space.bilibili.com/29325500"><img src="../icons/icon_bilibili.png"
                                    class="media-icon"></a>
                        </div>
                        <div class="media-link">
                            <a href="https://github.com/Frynoodles"><img src="../icons/github.png" class="media-icon"></a>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
    name: "header_pannel",
})
</script>

<style scoped lang="less">
// scoped 限制css只在当前作用域生效
// lang="less" 使用less，需要安装 npm install less-loader


.header {
    width: 100%;
    background-color: white;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;


    .header-content {
        display: flex;
        justify-content: space-evenly; // 水平方向 具体自己查
        align-items: center; // 垂直方向 居中
        width: 80%;
        height: 100%;

        .content-box {
            display: flex;
            justify-content: start; // 居左
            align-items: center; //侧轴居中
            flex-flow: row nowrap; //横向，不换行
        }

        .left-content {
            .logo {

                cursor: pointer; // 鼠标变手指样式

                img#header-logo {
                    height: 80px;
                }
            }
        }


        .center-content {
            display: flex;
            justify-content: center;
            width: 40%;
            height: 100%;

            .menu-bar {
                display: flex;
                justify-content: space-evenly;
                width: 70%;
                font-size: 40px;

                .menu-item {
                    display: flex;
                    align-items: center;

                    a {
                        text-decoration: none;
                        color: black;
                        font-size: 25px;
                        font-weight: bold;
                        font-family: "KuaiLe";
                    }
                }

                .dividing-line {
                    user-select: none;
                    height: 90%;
                    width: 1px;
                    background-color: black;
                }
            }
        }

        .right-content {
            width: 160px;

            .media-links {
                display: flex;
                align-items: center;
                justify-content: space-around;

                img.media-icon {
                    height: 40px;
                    width: 40px;
                }

                img#face-icon {
                    border-radius: 50%;
                    cursor: pointer;
                }
            }

        }


    }





}</style>