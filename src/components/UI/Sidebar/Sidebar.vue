<template>
  <div class="sidebar">
    <ul class="sidebar__menu">
      <li class="sidebar__item">
        <h3 class="sidebar__title">
          Заявки
        </h3>

        <Menu />
      </li>
      <li class="sidebar__item">
        <h3 class="sidebar__title">
          Контрагенты
        </h3>
      </li>
      <li class="sidebar__item">
        <h3 class="sidebar__title">
          Операторы
        </h3>
      </li>
      <li class="sidebar__item">
        <h3 class="sidebar__title">
          Статистика
        </h3>
      </li>
      <li class="sidebar__item">
        <h3 class="sidebar__title">
          Уведомления
        </h3>
      </li>
      <li class="sidebar__item">
        <h3 class="sidebar__title">
          Настройки
        </h3>
      </li>
    </ul>

    <div class="sidebar__btn">
      <Button title="Новое уведомление" :icon="false" />
    </div>
  </div>
</template>

<script>
import "./Sidebar.scss";
import Menu from "@/components/UI/Menu/Menu";
import Button from "@/components/UI/Button/Button";

export default {
  name: "Sidebar",
  components: {
    Menu,
    Button,
  },
};
</script>
