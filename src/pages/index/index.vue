<style scoped>
    .body{
        font-weight: 400;
        color: #333;
        font-size: 12px;
        background: #f3f3f3;
    }
    .header_index {
        position: relative;
        height: 36px;
        padding: 0px 0px;
        background: #fff;
        text-align: center;
    }

    .banner {
        padding: 0px 10px;
        margin-top: 10px;
    }
    .swiper image{
        width: 100%;
        height:180px;
        vertical-align:top;
    }

    .index_main {
        margin-top: 10px;
        padding: 0px 3px;
        overflow: hidden;
        height: auto;
    }
    .index_main .div01 {
        background: #fff;
        height: auto;overflow: hidden
    }

    .nav {
        padding-bottom: 20px;
    }

    .nav ul li{ float:left; display:inline; width:33%; text-align:center; margin-top:20px;}
    .nav ul li p{ text-align:center;}
    .nav ul li text{ text-align:center; display:block; color:#1d1d1d; line-height:20px; margin-top:5px; font-size:12px;}
    .nav ul li:hover text{ text-align:center; display:block; color:#ff5387; line-height:20px; margin-top:5px; font-size:12px;}
    .nav ul li:focus text{ text-align:center; display:block; color:#ff5387; line-height:20px; margin-top:5px; font-size:12px;}
    .nav ul li  img{ height:45px; width:45px;}

    .index_main .div02{ background:#fff; margin-top:10px; padding-bottom:20px;width: 100%;height: auto;overflow: hidden}
    .nav02 ul li{ float:left; display:inline; text-align:center; margin-top:20px; height:25px;}
    .nav02 ul li text{ display:inline-block; color:#1d1d1d; line-height:25px; font-size:12px; height:25px;}
    .nav02 ul li img{ float:left; display:inline; height:25px; width:25px;padding-left: 20px}
    .nav02 ul li  i{ padding-left:5px; font-style:normal;}
    .nav02 ul li:hover  i{ padding-left:5px; font-style:normal; color:#ff5387;}
    .nav02 ul li:focus  i{ padding-left:5px; font-style:normal; color:#ff5387;}
    .nav02 ul li:nth-child(1){ width:33%; min-width:120px;  padding-left:0px;}
    .nav02 ul li:nth-child(2){ min-width:90px; width:30%;  border-left:1px solid #dadada;  padding-left:0px;}
    .nav02 ul li:nth-child(3){ min-width:90px; width:30%;  border-left:1px solid #dadada;  padding-left:0px;}

</style>
<template>
    <div class="body">
        <div class="header_index">我要头像网</div>
        <div class="banner">
            <swiper class="swiper" indicator-dots="true" autoplay="true" interval="5000" duration="1000">
                <block v-for="(item, index) in imgUrls" :index="index" :key="key">
                    <swiper-item>
                        <image :src="item" class="slide-image" mode="aspectFit"/>
                    </swiper-item>
                </block>
            </swiper>
        </div>

        <div class="main index_main">
            <div class="div01 nav">
                <ul>
                    <li>
                        <a href="../photo/main">
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img01.png" alt="头像"></p>
                       头像
                        </a>
                    </li>
                    <li>
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img02.png" alt="网名"></p>
                        <a>网名</a>
                    </li>
                    <li>
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img03.png" alt="签名"></p>
                        <a>签名</a>
                    </li>
                    <li>
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img04.png" alt="分组"></p>
                        <a> 分组</a>
                    </li>
                    <li>
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img05.png" alt="图片"></p>
                        <a>图片</a>
                    </li>
                    <li>
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img06.png" alt="壁纸"></p>
                        <a>壁纸</a>
                    </li>
                    <li>
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img07.png" alt="排行"></p>
                        <a>排行</a>
                    </li>
                    <li>
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img08.png" alt="讨论组"></p>
                        <a> 讨论组 </a>
                    </li>
                    <li>
                        <p><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_img09.png" alt="商城"></p>
                        <a>商城</a>
                    </li>
                    <div class="clear"></div>
                </ul>
            </div>
            <div class="div02 nav02">
                <ul>
                    <li><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_pic01.png" alt="手机客户端"><i>手机客户端</i></li>
                    <li><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_pic02.png" alt="自拍"><i>自拍</i></li>
                    <li><img src="https://js.qzone.cc/v3/mobile-3.0/images/index_pic03.png" alt="日志"><i>日志</i></li>
                    <div class="clear"></div>
                </ul>

            </div>
        </div>
    </div>
</template>

<script>
  import card from '@/components/card'

  export default {
    data () {
      return {
        imgUrls: [
          '/static/images/5d5b4832aa18b364.jpg',
          '/static/images/5d5b4832aa18b364.jpg',
          '/static/images/5d5b4832aa18b364.jpg'
        ],
        indicatorDots: false,
        autoplay: false,
        interval: 5000,
        duration: 1000

      }
    },

    components: {
      card
    },

    methods: {
      bindViewTap () {
        const url = '../logs/main'
        if (mpvuePlatform === 'wx') {
          mpvue.switchTab({url})
        } else {
          mpvue.navigateTo({url})
        }
      },
      clickHandle (ev) {
        console.log('clickHandle:', ev)
        // throw {message: 'custom test'}
      },
      changeIndicatorDots: function (e) {
        this.setData({
          indicatorDots: !this.data.indicatorDots
        })
      },
      changeAutoplay: function (e) {
        this.setData({
          autoplay: !this.data.autoplay
        })
      },
      intervalChange: function (e) {
        this.setData({
          interval: e.detail.value
        })
      },
      durationChange: function (e) {
        this.setData({
          duration: e.detail.value
        })
      }
    },
    computed: {},

    mounted () {

    }
  }
</script>


