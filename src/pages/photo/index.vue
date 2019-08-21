<style scoped>
    .container {
        width: 100%;
        margin: 0px auto;
        position: relative;
        font-family: "微软雅黑";
    }

    .header {
        position: relative;
        height: 40px;
        padding: 0px 0px;
        background: #ff6f9e;
        text-align: center;
    }

    .header h1 {
        font-size: 16px;
        font-weight: 400;
        color: #fff;
        text-align: center;
        line-height: 40px;
    }

    /*返回按钮*/
    .back_btn {
        position: absolute;
        height: 20px;
        width: 30px;
        top: 50%;
        left: 10px;
        margin-top: -10px;
    }

    .back_btn img {
        height: 18px;
        width: auto;
        padding-left: 5px;
    }

    /*发布按钮*/
    .release_btn {
        position: absolute;
        height: 20px;
        width: 20px;
        top: 50%; /* right:10px; */
        margin-top: -10px;
    }

    .release_btn img {
        height: 18px;
        width: auto;
        padding-left: 5px;
    }
</style>
<template>
    <div class="container">
        <div class="header">
            <!--返回按钮-->
            <div class="back_btn"><img src="https://js.qzone.cc/v3/mobile-3.0/images/back_btn.png"></div>
            <h1>QQ头像</h1>
            <!--发布按钮-->
            <div class="right_btn release_btn"><img src="https://js.qzone.cc/v3/mobile-3.0/images/release_btn.png">
            </div>
        </div>
    </div>
</template>

<script>
  export default {
    data () {

    }
  }
</script>


