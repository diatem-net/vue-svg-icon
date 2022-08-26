<template>
  <svg :class="className" xmlns="http://www.w3.org/2000/svg">
    <use :xlink:href="`#${name}`" xmlns:xlink="http://www.w3.org/1999/xlink" />
  </svg>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  name: {
    type: String,
    required: true,
  },
  size: {
    type: String,
    default: null,
  },
})

const className = computed(() => {
  return `icon icon-${props.name} icon-${props.size}`
})
</script>

<style lang="scss" scoped>
// SIZE HELPER
@mixin size($width, $height: $width) {
  width: $width;
  height: $height;
}

// Default variables
$icon-size-xxs: 1.2rem !default;
$icon-size-xs: 1.6rem !default;
$icon-size-sm: 2rem !default;
$icon-size-base: 2.4rem !default;
$icon-size-lg: 2.8rem !default;
$icon-size-xl: 3.2rem !default;
$icon-size-xxl: 4rem !default;

.icon {
  display: inline-block;
  fill: currentColor;
  @include size($icon-size-base);
}

.icon-xxs {
  @include size($icon-size-xxs);
}

.icon-xs {
  @include size($icon-size-xs);
}

.icon-sm {
  @include size($icon-size-sm);
}

.icon-lg {
  @include size($icon-size-lg);
}

.icon-xl {
  @include size($icon-size-xl);
}

.icon-xxl {
  @include size($icon-size-xxl);
}
</style>
