<template>
  <section data-scroll-section>
    <div data-scroll data-scroll-call="itemAnimation" data-block-item>
      <hero />
    </div>
  </section>
</template>

<script>
import Hero from '../../Hero/Hero.vue'
export default { components: { Hero } }
</script>

<style scoped>
[data-scroll-section] {
  display: flex;
  padding: 30vh 5vw;
}

[data-block-item] {
  width: 100%;
  max-width: 30vw;
  background-color: #232323;
  height: 65vh;
  transform: scaleX(0);
  transform-origin: top left;
}
</style>
