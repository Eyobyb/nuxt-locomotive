<template>
  <div
    :class="{'border-primary':!brightBorder ,'border-customGray':brightBorder }"
    class="rounded-full bottom-2 font-inter border-2 max-w-min px-14 py-4 text-lg"
  >
    <slot />
  </div>
</template>

<script>
export default {
  props: {
    brightBorder: {
      type: Boolean,
      default: false
    }
  }
}
</script>