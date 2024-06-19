<!-- src/App.vue -->
<template>
  <div id="app">
    <TelegramLogin />
    <!-- Add your game component here -->
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import TelegramLogin from './components/TelegramLogin.vue';

export default defineComponent({
  name: 'App',
  components: {
    TelegramLogin
  }
});
</script>
