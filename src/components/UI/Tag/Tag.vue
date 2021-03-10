<template>
  <div class="tag">
    {{ title }}
  </div>
</template>

<script>
import "./Tag.scss";

export default {
  name: "tag",
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>
