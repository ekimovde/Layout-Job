<template>
  <div class="back-link">
    <i class="bx bx-left-arrow-alt back-link__icon"></i>
    <p class="back-link__text">{{ title }}</p>
  </div>
</template>

<script>
import "./BackLink.scss";

export default {
  name: "BackLink",
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>
