<template>
  <div class="hello">
    <home1 />
    <home2 />
    <home3 />
  </div>
</template>

<script>
import { Slider, SliderItem } from 'vue-easy-slider';
import home1 from './home1';
import home2 from './home2';
import home3 from './home3';

export default {
  name: 'HelloWorld',
  components: {
    Slider,
    SliderItem,
    home1,
    home2,
    home3,
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.sliderContainer {
  width: auto;
  height: 500px;
  z-index: 0;
}
.slide {
  width: 100%;
  height: 100%;
  background-size: 100%;
  background-repeat: no-repeat;
  background-color: #000;
  display: inline-block;
  vertical-align: middle;
}
.gotoDetail {
  background-image: #ff0000;
  background-size: cover;
  height: 50px;
  width: 130px;
  background-color: transparent;
  border-color: transparent;
  color: #3a2729;
}
.backpic{
  background-image: url("http://chairimg.deaso40.com/background/bigback.jpg");
  background-size: cover;
  background-position: 50% 50%;
}
.whiteborder{
  text-shadow:5px 2px 6px #000000;
  color: #ffffff
}
@media only screen and (max-width: "767px"){

}
</style>
