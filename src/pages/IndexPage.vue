<template>
  <q-page id="about" class="row items-center justify-evenly">
    <resume-page />
    <FloatingNavBar />
  </q-page>
</template>

<script setup lang="ts">
import ResumePage from 'pages/ResumePage.vue';
import FloatingNavBar from 'components/FloatingNavBar.vue';
</script>
