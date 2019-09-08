<template functional>
  <button
    :ref="data.ref"
    :class="[`btn-${props.size}`, data.class, data.staticClass]"
    :style="[data.style, data.staticStyle]"
    v-bind="data.attrs"
    v-on="listeners"
  >
    <slot/>
  </button>
</template>

<script>
export default {
  name: "base-button",
  props: {
    size: {
      type: String,
      default: 'small',
    }
  }
};
</script>