<template>
  <div class="table">
    <div class="table__container">
      <table class="table__main">
        <thead class="table__head">
          <tr class="table__tr">
            <th
              class="table__th"
              v-for="(item, index) in table.head"
              :key="index"
            >
              {{ item }}
            </th>
          </tr>
        </thead>

        <tbody class="table__body">
          <tr class="table__tr">
            <td
              class="table__td"
              v-for="(item, index) in table.last"
              :key="index"
            >
              {{ item }}
            </td>
          </tr>
        </tbody>

        <tbody class="table__body">
          <tr class="table__tr">
            <td
              class="table__td"
              v-for="(item, index) in table.new"
              :key="index"
            >
              {{ item }}
            </td>
          </tr>
        </tbody>
      </table>
    </div>

    <div class="table__info">
      <div class="table__item">
        Прошлый обьем:
        <span class="table__price table__price_last">
          5 321 745, 000
        </span>
      </div>

      <div class="table__item">
        Новый объем:
        <span class="table__price table__price_new">
          5 091 712, 000
        </span>
      </div>
    </div>

    <div class="table__buttons">
      <Button title="Принять изменения" :status="true" />
      <Button title="Отклонить изменения" :status="false" />
    </div>
  </div>
</template>

<script>
import "./Table.scss";
import Button from "@/components/UI/Button/Button";

export default {
  name: "Table",
  components: {
    Button,
  },
  props: {
    table: {
      type: Object,
      required: true,
    },
  },
};
</script>
