<template>
  <q-layout view="hHh lpR fFf">
    <q-page-container class="main-content">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup></script>

<style lang="scss">
.main-content {
  background: $background;
  color: $text;
  .intro {
    padding: 50px;

    .main-title {
      font-size: 2.5rem;
      color: $primary;
      margin: 20px 0;
    }

    .subtitle {
      font-size: 1.25rem;
      margin: 20px 0;
      color: $secondary;
    }
  }
}
</style>
