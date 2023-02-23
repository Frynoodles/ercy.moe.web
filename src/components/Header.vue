<script setup lang="ts">
// 按顺序执行，要放在前头
const searchText=()=>{
    (<HTMLInputElement>document.getElementById('search-ercy')).value = '点击测试';
}
</script>
<template>
    <div>
        <div class="header">
            <div class="header-content">

                <!-- 左侧 -->
                <div class="left-content">
                    <div class="logo item-wrapper  content-box">
                        <a href="http://ercy.moe/">
                            <img src="../icons/logo_beta_v0.3.png" alt="HideRua:没吃饭可以上厕所吗？" id="header-logo">
                        </a>
                    </div>
                </div>

                <!-- 中间 -->
                <div class="center-content">
                    <div class="menu-bar item-wrapper  content-box">
                        <div class="menu-item">
                            <a href="">首页</a>
                        </div>
                        <div class="menu-item">
                            <a href="">笔记</a>
                        </div>
                        <div class="menu-item">
                            <a href="">收藏</a>
                        </div>
                    </div>
                </div>

                <!-- 搜索框 -->
                <div class="search-box-wrapper">
                    <!-- 在这里放个搜索框吧 -->
                    <div class="search-box">
                        <input type="text" name="search-ercy" id="search-ercy">
                        <div class="button-box" @click="searchText"><img src="../icons/搜索.png"></div>
                    </div>
                </div>

                <!-- 音乐播放器 -->
                <div class="music-player-box">
                    <!-- 在这放个音乐播放器吧 -->
                </div>

                <!-- 右侧 -->
                <div class="right-content">
                    <div class="media-links item-wrapper content-box">

                        <div class="media-link">
                            <a href="https://space.bilibili.com/29325500"><img src="../icons/icon_bilibili.png"
                                    class="media-icon"></a>
                        </div>
                        <div class="media-link">
                            <a href="https://github.com/Frynoodles"><img src="../icons/github.png" class="media-icon"></a>
                        </div>
                        <div class="face">
                            <img src="../icons/face.jpg" class="media-icon" id="face-icon">
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>



<style scoped lang="less">
// scoped 限制css只在当前作用域生效
// lang="less" 使用less，需要安装 npm install less-loader


.header {
    width: 100%;
    background-color: white;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;


    .header-content {
        display: flex;
        justify-content: start; // 水平方向 具体自己查
        align-items: center; // 垂直方向 居中
        width: 85%;
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
            width: 20%;
            height: 100%;

            .menu-bar {
                display: flex;
                justify-content: space-evenly;
                width: 70%;

                .menu-item {
                    display: flex;
                    align-items: center;

                    a {
                        text-decoration: none;
                        color: rgba(0, 0, 0, 0.719);
                        font-size: 20px;
                        font-weight: lighter;
                        font-family: "KuaiLe";
                    }
                    a:hover{
                        color: aqua;
                    }
                }


            }
        }

        .music-player-box {
            height: 100%;
            width: 25%;
        }

        .search-box-wrapper {
            height: 100%;
            width: 35%;
            display: flex;
            align-items: center;

            .search-box {
                width: 100%;
                display: flex;
                justify-content: start;
                align-items: center;
                border-radius: 10px;
                border-style: none;
                background-color: rgba(0, 0, 0, 0.4);
                height: 35px;


                input#search-ercy {
                    height: 30px;
                    width: 100%;
                    padding-left: 5px;
                    background-color: rgba(255, 205, 205, 0);
                    border-style: none;
                    border-radius: 20px;
                    font-size: 18px;
                    outline: none;
                }

                .button-box {
                    height: 30px;
                    width: 30px;
                    margin: 10px;
                    background-color: rgba(0, 0, 0, 0);
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    img{
                        height: 20px;
                        width: 20px;
                    }
                    img:hover{
                        height: 25px;
                        width: 25px;
                    }
                }
            }

        }

        .right-content {
            width: 200px;

            .media-links {
                display: flex;
                align-items: center;
                justify-content: space-around;

                img.media-icon {
                    height: 30px;
                    width: 30px;
                }

                img#face-icon {
                    border-radius: 50%;
                    cursor: pointer;
                }
            }

        }


    }





}</style>