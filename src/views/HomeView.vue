<script setup lang="ts">
import { Header } from "@/widgets/header";
import { Footer } from "@/widgets/footer";
import { BottomTabNavigator} from "@/widgets/bottom-tab-navigator";
import { Content } from "@/shared/content";
import { MainCarousel } from "@/features/main-carousel";
</script>

<template>
  <Header/>
  <BottomTabNavigator/>
  <Content>
    <MainCarousel />
  </Content>
  <Footer />
</template>
