<script setup lang="ts">
(() => {
    window.onload = function () {
        // 添加事件监听，点击修改剪贴板
        for (let img of document.getElementsByClassName('decoration-img')) {
            (img as unknown as Element).addEventListener('click', async (e) => {
                await navigator.clipboard.writeText((img as unknown as Element).getAttribute('alt') || '');
            })
        }
    }
})();
</script>
<template>
    <div class="footer">
        <div class="decoration-footer">
            <div class="left-img-box">
                <img src="../icons/105575710_p0.png" alt="https://www.pixiv.net/artworks/105575710" class="decoration-img">
                <span id="hover-info">来源:https://www.pixiv.net/artworks/105575710(点击复制)</span>
            </div>
            <div class="right-img-box">
                <img src="../icons/102545983_p0.png" alt="https://www.pixiv.net/artworks/102545983" class="decoration-img">
                <span id="hover-info">来源:https://www.pixiv.net/artworks/105575710(点击复制)</span>
            </div>
        </div>
        <div class="info-footer"></div>
    </div>
</template>



<style scoped lang="less">
.footer {
    margin: 0%;
    padding: 0%;
    z-index: -1;

    .decoration-footer {
        font-size: 15px;
        color: pink;
        .left-img-box {
            position: fixed;
            bottom: 20px;
            left: 50px;
            display: flex;
            flex-direction: column;
            align-items: center;

            span {
                visibility: hidden;
            }

            img {
                height: 300px;
            }
        }

        .left-img-box:hover {
            span {
                visibility: visible;
            }
        }

        .right-img-box {
            position: fixed;
            bottom: 20px;
            right: 50px;
            display: flex;
            flex-direction: column;
            align-items: center;

            span {
                visibility: hidden;
            }

            img {
                height: 300px;
            }
        }

        .right-img-box:hover {
            span {
                visibility: visible;
            }
        }

    }
}
</style>