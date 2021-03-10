<template>
  <button class="button" :class="{ button__block_default: !icon }">
    <div class="button__block" v-if="icon">
      <i class="bx bx-check button__icon" v-if="status && icon" />

      <i class="bx bx-x button__icon" v-if="!status && icon" />
    </div>

    {{ title }}
  </button>
</template>

<script>
import "./Button.scss";

export default {
  name: "Button",
  props: {
    title: {
      type: String,
      required: true,
    },
    status: {
      type: Boolean,
      required: false,
    },
    icon: {
      type: Boolean,
      default: true,
    },
  },
};
</script>
