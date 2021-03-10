<template>
  <div class="plan">
    <PlanItem
      v-for="(plan, index) in plans"
      :key="index"
      :plan="plan"
      :index="index"
      :showItem="showItem"
      @onClickShow="onClickShow($event)"
    />
  </div>
</template>

<script>
import "./Plan.scss";
import PlanItem from "@/components/commons/PlanItem/PlanItem";

export default {
  name: "Plan",
  components: {
    PlanItem,
  },
  props: {
    plans: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      showItem: {
        index: 0,
        status: true,
      },
    };
  },
  methods: {
    onClickShow(index) {
      if (!this.showItem.status) {
        this.showItem.index = index;
        this.showItem.status = true;
      } else {
        if (index !== this.showItem.index) {
          this.showItem.index = index;
          this.showItem.status = true;
        } else {
          this.showItem.index = null;
          this.showItem.status = false;
        }
      }
    },
  },
};
</script>
