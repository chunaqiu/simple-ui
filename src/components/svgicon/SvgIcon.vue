<template>
  <svg class="svgicon" :class="{ 'loading-animation': loading }">
    <use :xlink:href="`#i-${iconname}`"></use>
  </svg>
</template>
<script>
import "./iconfont.js"
export default {
  name: "SSvgIcon",
  props: {
    iconname: {},
    loading: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
<style>
*{
  margin: 0;
  padding: 0;
}
@keyframes loading-animation {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
.loading-animation {
  animation: loading-animation 1s infinite linear;
}
.svgicon {
  height: 1em;
  width: 1em;
  vertical-align: middle;
  margin-right: 0.2em;
  margin-top: 3px;
}
</style>
