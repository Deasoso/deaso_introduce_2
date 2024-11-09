<template>
  <div>
    <div class="cardcontainer">
      <div class="fullwidth">
        <div class="fullheight">
          <div class="vermiddle">
            <div class="whiteback">
              <h2 class="subtitle blackfont">
                cn半糖咖啡，可以叫我coffee酱或者mio酱<br>
                <br>
                ⭐es：朔间凛月，天祥院英智梦女拒同担同嫁  *天祥院亲情向梦本人涉英/凪茨姐，副推/好感es大楼！<br>
                ⭐第五人格：约瑟夫单推！最多接受水仙/约骨（情亲向）拒摄殓摄（别贴脸就好）其他都无所谓*人屠双修但是两个都菜菜的，，<br>
                ⭐鬼灭之刃：时透单推，蛇恋姐！<br>
                ⭐弦音：竹早静弥单推<br>
                （*以上是以前混的浓度比较高的圈子，拒同担可能还有遗漏后续会慢慢补！）<br>
                <br>
                本人混圈比较杂基本什么番都看过，近期主要在搞es，es，排球，文野，弦音，女神异闻录浓度超高欢迎找我聊天！！（有推荐番可以告诉我！本人最近在填坑中！）<br>
                *除了es和以前一直搞的圈子其他不怎么拒同担哈！！<br>
                <br>
                目前正在自学日语还想搞点占卜什么的，<br>
              </h2>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    methods: {
      toMe() {
        document.getElementById('introduceme').scrollIntoView({ block: 'start', behavior: 'smooth' })
      },
      toGame(){
        this.$router.push("/games");
      },
      toMusic(){
        this.$router.push("/musics");
      },
      clickDownload(){
        this.$buefy.dialog.alert({
          title: '跳转',
          message: '<div>链接：</div><a href="https://www.tapechat.net/uu/90ZYPL/3XWRGVSM" target="_blank">https://www.tapechat.net/uu/90ZYPL/3XWRGVSM</a>',
          confirmText: '关闭'
        })
      }
    }
  }
</script>

<style scoped>
/*
  section 2
*/
.avatar{
  height: 132px;
  width: 132px;
  border-radius:50%;
  border: 3px solid white;
  vertical-align: top;
  display:inline-block;
  margin-bottom: 20px;
}
.cardcontainer{
  background-image: url("http://chairimg.deaso40.com/introduce/kafei_beijing2.jpg");
  background-size: cover;
  background-position: 50% 50%;
}
.whiteborder{
  text-shadow:5px 2px 6px #000000;
  color: #ffffff
}
.fullheight{
  height: 800px;
}
.fullwidth{
  max-width: 1280px;
  margin: auto;
}
.vermiddle{
  position: relative;
  top: 50%;
  transform: translateY(-50%);
}
.whiteback{
  margin-left: 30px;
  margin-right: 30px;
  padding: 30px;
  height: 620px;
  background-color: #ffffffbb;
  text-align: left;
}
.blackfont{
  color: #000000;
  font-size: 19px;
}

</style>