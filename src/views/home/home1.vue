<template>
  <div>
    <div class="cardcontainer">
      <div class="fullwidth">
          <div class="fullheight">
            <div class="vermiddle">
              <img class="avatar" src="http://chairimg.deaso40.com/introduce/kafei_touxiang.jpg"/>
              <h1 class="title whiteborder">
                咖啡
              </h1>
              <h2 class="subtitle whiteborder">
                老师蛞蝓这里coffee
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
  background-image: url("http://chairimg.deaso40.com/introduce/kafei_beijing.jpg");
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
}

</style>