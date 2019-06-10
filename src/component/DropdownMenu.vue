<template>
  <ul class="ms-doc-dropdown" :style="{ top: top + 'px'}">
    <li v-for="(value, key) in nav" class="ms-doc-dropdown__item">
      <a :href="value">{{ key }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'ms-doc-dropdown',

  props: {
    nav: Object,
    top: {
      type: Number,
      default: 0
    }
  }
};
</script>

<style lang="postcss">
@import '../style/variable';

.ms-doc-dropdown {
  position: absolute;
  top: 40px;
  right: 0px;
  padding: 8px 0;
  z-index: 10;
  background: #fff;
  border: 1px solid $ms-doc-border-color;
  text-align: left;
  border-radius: 4px;

  &__item {
    display: block;
    line-height: 2.2;
    font-size: 13px;
    letter-spacing: 1px;
    cursor: pointer;

    a {
      display: block;
      padding: 0 20px;
      color: $ms-doc-text-color;

      &:hover {
        color: $ms-doc-blue;
      }
    }
  }
}
</style>
