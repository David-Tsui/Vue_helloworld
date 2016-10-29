<template>
  <div class="section" id="page2">
    <button id="switch" v-on:click="show = !show">I am a switch~</button>
    <transition name="bounce">
      <p v-show="show">{{ msg }}</p>
    </transition>
    <p>小樓昨夜又東風</p>
    <p>故國不堪回首月明中</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'Page2!',
      show: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

p {
  font-size: 24px;
  color: #42b983;
}

.fade-enter-active, .fade-leave-active {
  animation: fly 1.6s forwards;
}
.fade-enter, .fade-leave-active {
  opacity: 0;
}

.bounce-enter-active {
  animation: bounce-in .5s;
}
.bounce-leave-active {
  animation: bounce-out .5s;
}

@keyframes fly {
  0% {
    opacity: 1;
    transform: translateX(0) translateY(0);
  }
  25% {
    transform: translateX(20px) translateY(15px);
  }
  50% {
    opacity: .65;
    transform: translateX(120px) translateY(0);
  }
  75% {
    transform: translateX(160px) translateY(-40px);
  }
  100% {
    opacity: 0;
    transform: translateX(200px) translateY(-30px);
  }
}

@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
@keyframes bounce-out {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(0);
  }
}

</style>
