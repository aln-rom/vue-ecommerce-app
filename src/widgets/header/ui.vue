<script lang="ts" setup>
import { Container } from "@/shared/container";
import { Logo } from '@/shared/logo';
import { Button } from '@/shared/button';

</script>

<template>
  <header class="header">
    <Container class="header__container">
      <div class="header__container__logo">
        <RouterLink to="/">
          <Logo orientation="horizontal" bgColor="white" colorful with-text/>
        </RouterLink>
      </div>
      
      <div class="header__container__button">
        <Button color="secondary">
          Каталог
        </Button>
      </div>
    </Container>
  </header>
</template>

<style scoped lang="scss">
.header {
  position: sticky;
  top: 0;
  left: 0;
  z-index: 1;
  
  &__container {
    display: flex;
    align-items: center;
    height: 72px;
    
    &__button {
      width: 140px;
      margin-left: 40px;
    }
  }
}
</style>
