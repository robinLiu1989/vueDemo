<template>
  <div id="example-2">
    <button @click="show = !show">Toggle show</button>
    <transition name="bounce">
      <p v-if="show">Look at me!</p>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      show: true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .bounce-enter-active {
    animation: bounce-in .5s;
  }
  .bounce-leave-active {
    animation: bounce-in .5s reverse;
  }
  @keyframes bounce-in {
    0% {
      transform: translateX(0) rotate(0);

    }
    50% {
      transform: translateX(100px) rotate(360deg);
    }
    100% {
      transform: translateX(0)  rotate(0);
    }
  }


</style>
