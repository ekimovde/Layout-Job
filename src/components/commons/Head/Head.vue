<template>
  <div class="head">
    <div class="head__nav">
      <BackLink title="Назад" />

      <a href="#" class="head__link">{{ company.status }}</a>
    </div>

    <div class="head__info">
      <div class="head__status">
        <h2 class="head__number">{{ company.number }}</h2>

        <Tag :title="company.tag" />
      </div>

      <div class="head__name">
        {{ company.name }}
      </div>
    </div>
  </div>
</template>

<script>
import "./Head.scss";
import Tag from "@/components/UI/Tag/Tag";
import BackLink from "@/components/UI/BackLink/BackLink";

export default {
  name: "Head",
  components: {
    Tag,
    BackLink,
  },
  props: {
    company: {
      type: Object,
      required: true,
    },
  },
};
</script>
