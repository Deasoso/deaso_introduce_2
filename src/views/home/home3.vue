<template>
  <div>
    <div class="cardcontainer">
      <div class="fullwidth">
        <div class="fullheight">
          <div class="vermiddle">
            <div class="whiteback">
              <h2 class="subtitle blackfont">
                本人INFJ 坐标南京外省长假会跑（随缘）<br>
                <br>
                工作日很少搞cos，基本行程都在长假<br>
                暂时只出少男少女呢<br>
                有一点点捏毛技能但不多哈。<br>
                周末可能跑跑水游城欢迎偶遇！！<br>
                <br>
                混过一段时间Kpop，但是浓度不高，，其实可以忽略不计（？）<br>
                <br>
                我素一个耳机不离身的人！有好听的歌也可以发给我！特别爱听！！<br>
                <br>
                手机基本在身边，消息看见都会回大概率秒回除了小部分时间没空<br>
                <br>
                游戏方面手机上只有偶像梦幻祭，第五人格和哈利波特，平常爱打点Switch（我素p5批！）也有玩点宝可梦（？）后续可能会入动森（穷穷的，）<br>
                以上。（可能有遗漏，有什么随时问！！）<br>
                <br>
                想加我的劳斯请点右上角！<br>
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
  background-image: url("http://chairimg.deaso40.com/introduce/kafei_beijing3.jpg");
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