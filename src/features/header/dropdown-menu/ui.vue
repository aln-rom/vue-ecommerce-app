<script lang="ts" setup>
import { RouterLink } from 'vue-router';
import { reactive } from "vue";
import { Container } from '@/shared/container';
import { Typography } from '@/shared/typography';

const catalog = reactive({
  sections: [
    { label: 'Молоко, сыр, яйцо', link: '/section' },
    { label: 'Напитки', link: '/section' },
    { label: 'Бакалея', link: '/section' },
    { label: 'Непродовольственные товары', link: '/section' },
    { label: 'Хлеб', link: '/section' },
    { label: 'Кондитерские изделия', link: '/section' },
    { label: 'Здоровое питание', link: '/section' },
    { label: 'Детское питание', link: '/section' },
    { label: 'Фрукты и овощи', link: '/section' },
    { label: 'Чай, кофе', link: '/section' },
    { label: 'Зоотовары', link: '/section' },
    { label: 'Мясо, птица, колбаса', link: '/section' },
    { label: 'Замороженные продукты', link: '/section' },
  ]
});
</script>

<template>
  <div class="dropdown-menu">
    <Container>
      <ul class="dropdown-menu__list">
        <li
          v-for="section in catalog.sections"
          :key="section.label"
          class="list__item"
        >
          <RouterLink :to="section.link">
            <Typography
              class="item__text"
              tagName="span"
              size="s"
              bold
            >{{ section.label }}</Typography>
          </RouterLink>
        </li>
      </ul>
    </Container>
  </div>
</template>

<style scoped>
.dropdown-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: var(--main-surface);
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.15);
  animation: .5s 1 forwards slideDown;
  opacity: 0;
}

.dropdown-menu__list {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-row-gap: 24px;
  grid-column-gap: 40px;
  padding: 40px 0;
}

.item__text:hover {
  color: var(--main-primary);
}

@keyframes slideDown {
  from {
    top: 0;
    opacity: 0;
  }
  to {
    top: 72px;
    opacity: 1;
  }
}
</style>
