<template>
  <div class="ms-doc-container ms-doc-row" :class="{ 'ms-doc-container--with-simulator': hasSimulator }">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'ms-doc-container',

  props: {
    hasSimulator: Boolean
  }
};
</script>

<style lang="postcss">
@import '../style/variable';

.ms-doc-container {
  overflow: hidden;
  box-sizing: border-box;
  background-color: #fff;
  padding-left: $ms-doc-nav-width;

  &--with-simulator {
    padding-right: calc($ms-doc-simulator-width + $ms-doc-padding);

    @media (max-width: 1300px) {
      padding-right: calc($ms-doc-simulator-small-width + $ms-doc-padding);
    }
  }
}
</style>
