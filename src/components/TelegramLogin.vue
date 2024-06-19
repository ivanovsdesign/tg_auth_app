<!-- src/components/TelegramLogin.vue -->
<template>
  <div ref="telegramLogin"></div>
</template>

<script lang="ts">
import { defineComponent, onMounted, ref } from 'vue';

export default defineComponent({
  name: 'TelegramLogin',
  setup() {
    const telegramLogin = ref(null);

    onMounted(() => {
      const script = document.createElement('script');
      script.src = 'https://telegram.org/js/telegram-widget.js?7';
      script.async = true;
      script.setAttribute('data-telegram-login', 'YOUR_BOT_USERNAME');
      script.setAttribute('data-size', 'large');
      script.setAttribute('data-auth-url', 'http://localhost:5000/auth/telegram');
      script.setAttribute('data-request-access', 'write');
      telegramLogin.value.appendChild(script);
    });

    return {
      telegramLogin
    };
  }
});
</script>
