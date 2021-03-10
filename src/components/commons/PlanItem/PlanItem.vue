<template>
  <div class="plan-item">
    <div class="main" @click="$emit('onClickShow', index)">
      <div class="main__info">
        <div class="main__contract" v-for="(tmp, id) in plan.info" :key="id">
          <span class="main__title">{{ tmp.title }}</span>

          <p class="main__descr">{{ tmp.descr }}</p>
        </div>
      </div>

      <Status :status="plan.status.info" :title="plan.status.title" />
    </div>

    <Table
      v-if="index === showItem.index && showItem.status"
      :table="plan.table"
    />
  </div>
</template>

<script>
import "./PlanItem.scss";
import Status from "@/components/UI/Status/Status";
import Table from "@/components/commons/Table/Table";

export default {
  name: "PlanItem",
  components: {
    Status,
    Table,
  },
  props: {
    plan: {
      type: Object,
      required: true,
    },
    showItem: {
      type: Object,
      required: false,
    },
    index: {
      type: Number,
      required: true,
    },
  },
};
</script>
