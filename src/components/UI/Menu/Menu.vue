<template>
  <ul class="menu">
    <li class="menu__item">
      <p class="menu__text">
        В работе
      </p>
      128
    </li>
    <li class="menu__item">
      <p class="menu__text">
        Истекает срок
      </p>
      3
    </li>
    <li class="menu__item menu__item_active">
      <p class="menu__text">
        Просрочены
      </p>
      4
    </li>
  </ul>
</template>

<script>
import "./Menu.scss";

export default {
  name: "Menu",
};
</script>
