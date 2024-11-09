<template>
  <div class="header">
    <div class="navbar is-fixed-top nav-shadow" :style="{ backgroundColor: tweenedCSSColor }">
    </div>
    <div>
      <nav class="navbar is-fixed-top headerwidth" role="navigation" aria-label="main navigation">
        <div class="navbar-brand">
          <a class="navbar-item" @click="$router.push('/')">
            <img class="logoimg" src="http://chairimg.deaso40.com/introduce/kafei_touxiang.jpg">
          </a>
          <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample" ref="nav" @click="clicknav">
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </a>
        </div>

        <div id="navbarBasicExample" class="navbar-menu" ref="navitem" :style="{ backgroundColor: secondTweenedCSSColor }">
          <!-- <div class="navbar-start">
            <a class="navbar-item whitefont" @click="clickDownload()">
              留言板
            </a>
          </div> -->

          <div class="navbar-end">
            <div class="navbar-item">
              <b-button type="is-light" outlined @click="clickCall()">联系方式</b-button>
            </div>
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
var Color = net.brehaut.Color

export default {
  data() {
    return {
      selected: "",
      title: "",
      color: {
        red: 255,
        green: 255,
        blue: 255,
        alpha: 0
      },
      tweenedColor: {},
      colorshowing: false,
    }
  },
  mounted(){
    window.addEventListener('scroll', this.handleScroll);
  },
  created: function () {
    this.tweenedColor = Object.assign({}, this.color)
  },
  methods: {
    clicknav(){
      // console.log(this.$refs.nav.classList);
      this.$refs.nav.classList.toggle("is-active");
      this.$refs.navitem.classList.toggle("is-active");
    },
    handleScroll(){
      const top = document.documentElement.scrollTop || window.pageYOffset || document.body.scrollTop;
      if (top > 60 && !this.colorshowing) {
        this.color = new Color({
          red: 0,
          green: 0,
          blue: 0,
          alpha: 0.6
        }).toRGB();
        this.colorshowing = true;
      } else if (top <= 59 && this.colorshowing){
        this.color = new Color({
          red: 0,
          green: 0,
          blue: 0,
          alpha: 0
        }).toRGB();
        this.colorshowing = false;
      }
    },
    clickDownload(){
      this.$buefy.dialog.alert({
        title: '跳转',
        message: '<div>链接：</div><a href="https://www.tapechat.net/uu/90ZYPL/3XWRGVSM" target="_blank">https://www.tapechat.net/uu/90ZYPL/3XWRGVSM</a>',
        confirmText: '关闭'
      })
    },
    clickCall(){
      this.$buefy.dialog.alert({
        title: 'wx二维码',
        message: '<div><img class="avatar" style="max-width: 200px;margin-left: calc(50% - 100px);" src="http://chairimg.deaso40.com/introduce/kafei_weixin.jpg"/></div>',
        confirmText: '关闭'
      })
    }
  },
  watch: {
    color: function () {
      function animate () {
        if (TWEEN.update()) {
          requestAnimationFrame(animate)
        }
      }
      new TWEEN.Tween(this.tweenedColor)
        .to(this.color, 100)
        .start()
      animate()
    }
  },
  computed: {
    tweenedCSSColor: function () {
      // console.log(new Color({
      //   red: this.tweenedColor.red,
      //   green: this.tweenedColor.green,
      //   blue: this.tweenedColor.blue,
      //   alpha: this.tweenedColor.alpha
      // }).toCSS());
      if(this.tweenedColor.alpha == 1){
        return "rgba(0,0,0,1)";
      }else{
        return new Color({
          red: this.tweenedColor.red,
          green: this.tweenedColor.green,
          blue: this.tweenedColor.blue,
          alpha: this.tweenedColor.alpha
        }).toCSS()
      }
    },
    secondTweenedCSSColor: function() {
      if(document.body.clientWidth < 1024){
        if(this.tweenedColor.alpha == 1){
          return "rgba(0,0,0,1)";
        }else{
          return new Color({
            red: this.tweenedColor.red,
            green: this.tweenedColor.green,
            blue: this.tweenedColor.blue,
            alpha: this.tweenedColor.alpha
          }).toCSS()
        }
      }else{
        return "rgba(0,0,0,0)";
      }
    }
  },
}
</script>
<style scoped>
.header{
  z-index: 1000;
}
.logoimg{
  margin-left:8px;
  margin-right:16px;
  width:28px; 
  height:28px;
  /* padding: 2px; */
  border-radius:50%;
  /* border: 1px solid black; */
}
.headerwidth{
  text-align: center;
  max-width: 1280px;
  background: none;
  margin:auto;
}
.whitefont{
  padding-left: 20px;
  padding-right: 20px;
  color: #ffffff;
}
.nav-shadow{
  box-shadow: 0px 0px 10px 0px #acacac;
  height:56px;
  background: #000000;
}
@media screen and (max-width: 1023px){
  .navbar-menu {
    background-color: rgba(0, 0, 0, 0);
  }
}
</style>

