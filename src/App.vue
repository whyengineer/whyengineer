<template>
  <div>
    <Nav></Nav>
    <Slider></Slider>
    <div class="line"></div>
    <HC></HC>
  </div>
</template>

<script>
import Nav from './Nav.vue'
import Slider from './Slider.vue'
import HC from './HomeC.vue'

export default {
  components:{
    Nav,
    Slider,
    HC
  },
  name: 'app',
  data () {
  }
}
</script>

