<template>
  <div class="basic-transition">
    <div class="text-container" @click="on = !on">
      <transition
        enter-active-class="animated bounceInLeft"
        leave-active-class="animated bounceOutRight"
      >
        <div v-if="on" key="on">On</div>
        <div v-else>Off</div>
      </transition>
    </div>
    <p>Click on the text to toggle it</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      on: true,
    }
  },
}
</script>

<style scoped>
.text-container {
  cursor: pointer;
  text-align: left;
  padding: 1rem;
}

.animated.bounceOutRight {
  position: absolute;
}

.basic-transition {
  font-size: 1.5rem;
}
</style>
