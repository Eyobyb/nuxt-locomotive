<template>
  <div class="relative w-screen h-screen flex justify-center items-center">
    <div class="absolute left-5 top-5">
      <logo />
    </div>

    <!-- <div
      class="h-screen sm:h-min sm:w-1/2 height-maxer w-full flex flex-col items-center justify-end sm:relative top-0 py-4 px-2"
    >
      <div class="relative flex flex-col items-center gap-7">
        <eyob-amharic class="absolute -top-20" />
      </div>
    </div>-->
    <div class="relative">
      <div class="absolute left-8 bottom-5">
        <div class="relative">
          <eyob-amharic
            data-svg-title
            class="transform z-[-1] w-full absolute -top-40 -left-14 opacity-0"
          />
          <div
            class="z-20 text-center sm:text-start text-primary flex flex-col gap-2 max-w-[650px]"
          >
            <h1 class="text-4xl md:text-8xl font-fam-inter font-bold text-primary">Eyob Yirgu</h1>
            <h2
              class="text-3xl md:text-5xl font-bold font-fam-inter text-primary"
            >Full Stack Developer.</h2>
            <p
              class="font-fam-raleway text-2xl font-medium text-[#525252]"
            >I’m a software engineer based in Addis Ababa , Ethiopia specialized in building websites (and occasionally designing) .</p>
          </div>

          <primay-button class="mt-5 w-80">Resume</primay-button>
        </div>
      </div>
      <background />
    </div>
  </div>
</template>

<script>
import Logo from '../../components/Logo.vue'
import Background from '../../components/Background.vue'
import PrimayButton from '../../components/PrimayButton.vue'
import EyobAmharic from '../../components/EyobAmharic.vue'
export default {
  components: [],
  methods: {},
  components: { Logo, Background, PrimayButton, EyobAmharic }
}
</script>
