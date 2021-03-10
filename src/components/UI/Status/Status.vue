<template>
  <div class="status">
    <div
      class="status__circle"
      :class="{
        status__circle_adopted: status === 'adopted',
        status__circle_rejected: status === 'rejected',
      }"
    >
      <i class="bx bx-check status__icon" v-if="status === 'adopted'" />
      <i class="bx bx-x status__icon" v-if="status === 'rejected'" />
    </div>
    <span class="status__text">
      {{ title }}
    </span>
  </div>
</template>

<script>
import "./Status.scss";

export default {
  name: "Status",
  props: {
    status: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
};
</script>
