<style scoped>
    .container{ max-width:640px; /*width:320px;*/ margin:0px auto; position:relative; font-family:"微软雅黑";}
    /*头部*/
    .header{ position:relative; height:40px; padding:0px 0px; background:#ff6f9e; text-align:center;}
    .header h1{ font-size:16px; font-weight:400; color:#fff; text-align:center; line-height:40px;}

    /*返回按钮*/
    .back_btn{ position:absolute; height:20px; width:30px; top:50%; left:10px; margin-top:-10px;}
    .back_btn a{ display:inline-block; width:20px; height:20px; text-decoration:none;}
    .back_btn a image{ height:18px; width:10px; padding-left:5px;}

    /*发布按钮*/
    .release_btn{ position:absolute; height:20px; width:20px; top:50%;/* right:10px; */ margin-top:-10px; }
    .release_btn a{ display:block; width:20px; height:20px;}
    .release_btn a image{ height:18px; width:15px; padding-left:5px;}

    /*分享按钮*/
    .share_btn{ position:absolute; height:20px; width:20px; top:50%; /*right:10px;*/ margin-top:-10px; }
    .share_btn a{ display:block; width:20px; height:20px; }
    .share_btn a image{ height:18px; width:10px; padding-left:5px;}

    /*跳转按钮*/
    .goto_btn{ position:absolute; height:20px; width:20px; top:50%; /*right:10px;*/ margin-top:-10px; }
    .goto_btn a{ display:block; width:20px; height:20px; }
    .goto_btn a image{ height:18px; width:10px; padding-left:5px;}

    .header .right_btn:nth-last-child(1){ right:10px;}
    .header .right_btn:nth-last-child(2){ right:40px; }

    /*下拉菜单01*/
    .sub_nav01{ display:none;}
    .sub_nav01{ position:absolute; z-index:999; width:100%; max-width:640px; border-top:1px solid #dcdfec; background-color:#fff; padding-top:5px;}
    .sub_nav01 dl{ margin-top:5px;}
    .sub_nav01 dl dt{ text-align:center; padding:0px 20px; color:#ff6f9e; font-size:12px;}
    .sub_nav01 dl span{ float:left; display:inline-block; width:25%; padding:0px 10px; height:20px; line-height:20px; margin-top:0px; text-align:center; margin-top:5px;}
    .sub_nav01 dl span a{ display:block; width:100%; color:#6d6d6d; background:#f3f3f3; border-radius:10px; line-height:20px;}
    .sub_nav01 dl span a:hover{ display:block; width:100%; color:#fff; background:#ff97b9; border-radius:10px; line-height:20px;}
    .sub_nav01 dl span.active a{ display:block; width:100%; color:#fff; background:#ff97b9; border-radius:10px; line-height:20px;}

    .sub_nav_close_btn{ height:30px; padding-top:5px; text-align:center;}
    .sub_nav_close_btn img{ height:10px; width:auto;}
    .sub_nav_mark{ width:100%; height:100%; max-width:640px; bottom:0px; top:76px;  position:fixed; z-index:998; background:#000; opacity:.5;}
    /*导航01*/
    .nav01{ height:32px; background:#fff; border-bottom:1px solid #dcdfec;}
    .nav01 ul li{ float:left; display:inline; width:20%; text-align:center;}
    .nav01 ul li a{ display:inline-block; line-height:31px; height:31px; padding:0px 10px; color:#919191; border-bottom:1px solid #fff; font-size:13px;}
    .nav01 ul li a:hover{ color:#ff6f9e; border-bottom:1px solid #ff6f9e;}
    .nav01 ul li a:focus{ color:#ff6f9e; border-bottom:1px solid #ff6f9e;}
    .nav01 ul li.active a{ color:#ff6f9e; border-bottom:1px solid #ff6f9e;}
    .nav01 ul li.more{float:right;}

    .nav01 ul h3{ float:left; display:block;line-height:32px; height:32px; padding:0px 10px; color:#ff6f9e;font-size:13px;}

    /*导航04*/
    .nav04{ height:32px; background:#fff; border-bottom:1px solid #dcdfec;}
    .nav04 ul li{ float:left; display:inline; width:12.5%; text-align:center;}
    .nav04 ul li a{ display:inline-block; line-height:31px; height:31px; padding:0px 3px; color:#919191; border-bottom:1px solid #fff; font-size:13px;}
    .nav04 ul li a:hover{ color:#ff6f9e; border-bottom:1px solid #ff6f9e;}
    .nav04 ul li a:focus{ color:#ff6f9e; border-bottom:1px solid #ff6f9e;}
    .nav04 ul li.active a{ color:#ff6f9e; border-bottom:1px solid #ff6f9e;}

    /*导航05*/
    /*.nav05 ul li{ float:left; display:inline; width:25%; height:40px; line-height:40px; text-align:center;}*/
    .nav05 ul li{ float:left; display:inline; width:20%; height:40px; line-height:40px; text-align:center;}
    .nav05 ul li a{ display:block; text-align:center; color:#777;}
    .nav05 ul li.active a{ background:#d1d9de; color:#fff;}

    /*导航06*/
    .nav06 ul li{ float:left; display:inline; width:25%; height:36px;  text-align:center; padding:3px 0px;}
    .nav06 ul li a{ display:block; width:100%; text-align:center; color:#777; border-left:1px solid #e5e5e5; line-height:30px;}
    .nav06 ul li.active{ background:#d1d9de;}

    /*导航07*/
    .nav07 ul li{ float:left; display:inline; width:25%; height:38px;  text-align:center; padding:4px 0px; background:#ff6f9e;}
    .nav07 ul li a{ display:block; width:100%; text-align:center; color:#fff; border-left:1px solid #f491b6; line-height:30px; font-size:14px;}
    .nav07 ul li.active{ background:#ff538b;}

    /*导航08*/
    .nav08 ul li{ float:left; display:inline;  height:35px; line-height:35px; text-align:center;}
    .nav08 ul li a{ display:inline-block; padding:0px 8px; text-align:center; color:#777;}
    .nav08 ul li.active a{ background:#d1d9de; color:#fff;}

    /*导航09*/
    .nav09 ul li{ float:left; display:inline; width:25%; height:52px;  text-align:center; padding:4px 0px; background:#ff6f9e;}
    .nav09 ul li p{width:100%; text-align:center; border-left:1px solid #f491b6; padding-top:2px; }
    .nav09 ul li a{ display:block; line-height:22px; font-size:14px; color:#fff; }
    .nav09 ul li.active{ background:#ff538b;}


    /*04qq头像*/
    .qqhead_list{ padding:0px 10px 10px; margin-top:0px;}
    .qqhead_list h2{ padding:0px 10px; line-height:32px; color:#ababab; padding-top:4px;}
    .qqhead_list_box{ margin-top:10px; background:#fff;}
    .qqhead_list_box h3{ padding:0px 10px; height:32px;line-height:32px; color:#777; padding-top:4px;}
    .qqhead_list_box h3 a{color:#777;line-height:32px;font-weight: bold;font-size: 0.8em}
    .qqhead_list_box .div01{text-align:center;}
    .qqhead_list_box .div01 ul{ margin-left:0px; margin-top:-5px;text-align:center;}
    .qqhead_list_box .div01 ul li{ float:left; display:block; width:45.5%; margin-left:10px; margin-top:10px;text-align:center;}
    .qqhead_list_box .div01 ul li > a{ display:inline-block;}
    .qqhead_list_box .div01 ul li > a img{width:165px; height:165px;}
    .qqhead_list_box .div02{ height:50px; margin-top:10px; padding:0px 10px;overflow: hidden}
    .qqhead_list_box .div01 ul li p{ margin-top:5px;}
    .qqhead_list_box .div01 ul li > img{width:165px;height:165px;}
    .qqhead_list_box .div01 ul li p a{ line-height:20px; color:#777777;}
    .qqhead_list_box .div01 ul li p a:hover{ line-height:20px; color:#ff6f9e;}

    .qqhead_list_box .pic ul{margin:-10px 10px 0 10px;}
    .qqhead_list_box .pic ul li{ float:left; display:block; width:100%; margin-left:0px; margin-top:10px;text-align:center;}
    .qqhead_list_box .pic ul li > a{ display:inline-block;}
    .qqhead_list_box .pic ul li > a img{width:140px; height:140px;}
    /*.qqhead_list_box .pic ul li > a img{ width:370px;height:auto;}*/

    .qqhead_list_box .content {}
    .qqhead_list_box .content ul{margin:-10px 10px 0 10px;}
    .qqhead_list_box .content ul li{ display:block; min-width:280px; margin-left:0px; margin-top:10px;text-align:center;}
    .qqhead_list_box .content ul li > img{width:200px; height:200px;}
    .qqhead_list_box .content ul li > a{ display:inline-block;}
    .qqhead_list_box .content ul li > a img{ width:280px; height:280px; }
    /*.qqhead_list_box .content ul li > a img{ min-width:280px;max-width:600px; height:auto; }*/

    .loading{display:block;margin:20px auto;text-align:center;height:200px;line-height:200px;}

    /*会员评论 点赞*/
    .member_comment{}
    .member_comment em{font-style:normal;}
    .member_comment .l{ float:left; display:block; margin-left:0px; margin-top:5px; height:32px; width:200px;}
    .member_comment .l img{float:left; height:31px; width:31px;margin-right:5px;}
    .member_comment .l p{float:left; display:block; margin-left:0px;line-height:16px;}
    .member_comment .l p em{font-size:12px; color:#777; font-style:normal; font-weight:400;}
    .member_comment .l p span{display:block;font-size:10px;color:#ababab;line-height:16px;height:16px;white-space:nowrap;}
    .member_comment .r{ float:right; display:block; margin-right:0px; margin-top:0px; height:32px;}
    .member_comment .r li{float:left; display:block; width:29px;max-width:29px; color:#919191; line-height:20px; text-align:center; font-size:10px;margin-left:10px;}
    .member_comment .r li .pic{ display:block; width:29px; height:22px;}
    .member_comment .r li .pic img{ height:22px; width:22px;text-align:center;}
    .member_comment .r li .number{ display:block;margin:0 auto; width:29px; height:22px;text-align:center;}
    .member_comment .r li em{font-style:normal;font-weight:400;}
    .member_comment .r span{ display:inline-block; width:22px; color:#919191; line-height:20px; text-align:center; font-size:10px;}
    .member_comment .r span a{ display:block; width:22px; height:22px;}
    .member_comment .r span a img{ height:22px; width:22px;}
    .member_comment .r span.span02{ margin-left:10px;}
    .member_comment .r span.span03{ margin-left:10px;}

    /*下拉菜单01*/
    .sub_nav01{ display:none;}
    .sub_nav01{ position:absolute; z-index:999; width:100%; max-width:640px; border-top:1px solid #dcdfec; background-color:#fff; padding-top:5px;}
    .sub_nav01 dl{ margin-top:5px;height: auto;overflow: hidden}
    .sub_nav01 dl dt{ text-align:center; padding:0px 20px; color:#ff6f9e; font-size:12px;}
    .sub_nav01 dl span{ float:left; display:inline-block; width:25%; padding:0px 10px; height:20px; line-height:20px; margin-top:0px; text-align:center; margin-top:5px;}
    .sub_nav01 dl span a{ display:block; width:100%; color:#6d6d6d; background:#f3f3f3; border-radius:10px; line-height:20px;}
    .sub_nav01 dl span a:hover{ display:block; width:100%; color:#fff; background:#ff97b9; border-radius:10px; line-height:20px;}
    .sub_nav01 dl span.active a{ display:block; width:100%; color:#fff; background:#ff97b9; border-radius:10px; line-height:20px;}

    .sub_nav_close_btn{ height:30px; padding-top:5px; text-align:center;}
    .sub_nav_close_btn img{ height:10px; width:25px;}
    .sub_nav_mark{ width:100%; height:100%; max-width:640px; bottom:0px; top:76px;  position:fixed; z-index:998; background:#000; opacity:.5;}
</style>
<template>
    <div class="container">
        <div class="header">
            <!--返回按钮-->
            <div class="back_btn"><a href="/"><img src="https://js.qzone.cc/v3/mobile-3.0/images/back_btn.png"></a></div>
            <h1>QQ头像</h1>
            <!--发布按钮-->
            <div class="right_btn release_btn"><a href="/qqtouxiang/add"><img src="https://js.qzone.cc/v3/mobile-3.0/images/release_btn.png"></a></div>
        </div>
        <div class="nav01" style="position:relative;">
            <ul>
                <li class="active"><a href="/qqtouxiang/">最新</a></li>
                <li><a href="/qqtouxiang/nvsheng/">女生</a></li>
                <li><a href="/qqtouxiang/nansheng/">男生</a></li>
                <li><a href="/qqtouxiang/aiqing/">情侣</a></li>
                <li class="more"><a @click="sel">更多</a></li>
            </ul>
            <div class="clear"></div>
            <div class="sub_nav01" :style="{display:first}">
                <dl>
                    <dt>排行</dt>
                    <dd>
                        <span><a href="/qqtouxiang/hot/">今日热门</a></span>
                        <span class="active"><a href="/qqtouxiang/">今日最新</a></span>
                        <span><a href="/qqtouxiang/recommend/">小编推荐</a></span>
                        <span><a href="/qqtouxiang/day/">今日排行</a></span>
                        <span><a href="/qqtouxiang/week/">本周排行</a></span>
                        <span><a href="/qqtouxiang/month/">本月排行</a></span>
                        <span><a href="/qqtouxiang/fav/">热门收藏</a></span>
                        <!-- <span><a href="/qqtouxiang/dz/">单张精选</a></span> -->
                        <span><a href="/zt/qqtouxiang/">头像专题</a></span>
                        <div class="clear"></div>
                    </dd>
                </dl>
                <dl>
                    <dt>分类</dt>
                    <dd>
                        <span class="active"><a href="/qqtouxiang/">全部分类</a></span>
                        <span><a href="/qqtouxiang/nvsheng/">女生头像</a></span>
                        <span><a href="/qqtouxiang/nansheng/">男生头像</a></span>
                        <span><a href="/qqtouxiang/aiqing/">情侣头像</a></span>
                        <span><a href="/qqtouxiang/oumei/">欧美头像</a></span>
                        <span><a href="/qqtouxiang/katong/">动漫头像</a></span>
                        <span><a href="/qqtouxiang/wenzi/">文字头像</a></span>
                        <span><a href="/qqtouxiang/mingxing/">明星</a></span>
                        <div class="clear"></div>
                    </dd>
                </dl>
                <dl>
                    <dt>标签</dt>
                    <dd>
                        <span><a href="/qqtouxiang/nvsheng/古风/">古风</a></span>
                        <span><a href="/qqtouxiang/nvsheng/部位/">部位</a></span>
                        <span><a href="/qqtouxiang/nvsheng/ins/">ins</a></span>
                        <span><a href="/qqtouxiang/nvsheng/女神/">女神</a></span>
                        <span><a href="/qqtouxiang/nvsheng/日系/">日系</a></span>
                        <span><a href="/qqtouxiang/nvsheng/伤感/">伤感</a></span>
                        <span><a href="/qqtouxiang/nvsheng/意境/">意境</a></span>
                        <span><a href="/qqtouxiang/nvsheng/韩系/">韩系</a></span>
                        <span><a href="/qqtouxiang/nvsheng/swag/">swag</a></span>
                        <span><a href="/qqtouxiang/nvsheng/闺蜜/">闺蜜</a></span>
                        <span><a href="/qqtouxiang/nvsheng/小清新/">小清新</a></span>
                        <span><a href="/qqtouxiang/nansheng/丧/">丧</a></span>
                        <span><a href="/qqtouxiang/oumei/重口味/">重口味</a></span>
                        <span><a href="/qqtouxiang/nansheng/半身/">半身</a></span>
                        <span><a href="/qqtouxiang/nvsheng/海边/">海边</a></span>
                        <span><a href="/qqtouxiang/nvsheng/学生党/">学生党</a></span>
                        <div class="clear"></div>
                    </dd>
                </dl>      <div class="sub_nav_close_btn"> <a @click="re"><img src="/static/images/sub_nav_close.jpg" alt=""></a> </div>
            </div>
            <div class="sub_nav_mark" :style="{display:second}"></div>
        </div>
        <div class="main qqhead" style="padding-bottom:85px;">
            <div class="qqhead_list" id="randomDiv">


                <div class="qqhead_list_box">
                    <h3>
                        <a href="/qqtouxiang/nvsheng/2945129.html">谁能凭爱意要富士山私有</a>
                    </h3>
                    <div class="div01">
                        <ul>
                            <li>
                                <a href="/qqtouxiang/nvsheng/2945129.html"><img
                                        class="lazy" src="/static/images/5d6676551165c631.jpg"
                                      ></a>
                            </li>
                            <li>
                                <a href="/qqtouxiang/nvsheng/2945129.html"><img
                                        class="lazy" src="/static/images/5d6676551165c631.jpg"
                                ></a>
                            </li>
                        </ul>
                        <div class="clear"></div>
                    </div>

                    <div class="div02 member_comment">
                        <div class="l">
                            <a href="/u/3067618">
                                <img src="/static/images/18.jpg!60x60.jpg"/>
                            </a>
                            <p>
                                <a href="/u/3067618"><em>久一</em></a>
                                <br>
                                <span>今天 20:43</span>
                            </p>
                        </div>
                        <div class="r">
                            <li onclick="vote.actvote(this,'avatar',2945129,'like');">
                                <span class="pic"><img src="https://js.qzone.cc/v3/mobile-3.0/images/qqhead_icon01.png"></span>
                                <span class="number">(0)</span>
                            </li>
                            <li onclick="vote.actvote(this,'avatar',2945129,'fav');">
                                <span class="pic"><img src="https://js.qzone.cc/v3/mobile-3.0/images/qqhead_icon03.png"></span>
                                <span class="number">(0)</span>
                            </li>
                        </div>
                        <div class="clear"></div>
                    </div>



                    <!--  固定位广告结束-->

            </div>
            </div>
        </div>
    </div>
</template>

<script>
  export default {
    data () {
      return {
        first: 'none',
        second: 'none'
      }
    },
    methods: {
      sel: function () {
        this.first = 'block'
        this.second = 'block'
      },
      re: function () {
        this.first = 'none'
        this.second = 'none'
      }
    }
  }
</script>


