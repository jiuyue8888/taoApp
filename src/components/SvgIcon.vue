<template>
  <svg
    :class="svgClass"
    aria-hidden="true"
    :width="size.split(',')[0] + 'px'"
    :height="size.split(',')[1] + 'px'"
  >
    <use :xlink:href="iconName"></use>
  </svg>
</template>

<script>
export default {
  name: "svg-icon",
  props: {
    iconClass: {
      type: String,
      required: true
    },
    className: {
      type: String
    },
    size: {
      type: String,
      default: "24,24"
    }
  },
  computed: {
    iconName() {
      return `#icon-${this.iconClass}`;
    },
    svgClass() {
      if (this.className) {
        return "svg-icon " + this.className;
      } else {
        return "svg-icon";
      }
    }
  }
};
</script>

<style scoped>
.svg-icon {
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
</style>
