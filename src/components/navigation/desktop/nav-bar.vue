<template>
  <div class="nav-bar__buttons">
    <template v-if="!isAuthenticated">
      <SignupButton />
      <LoginButton />
    </template>
    <template v-if="isAuthenticated">
      <logoutButton />
    </template>
    <nav class="nav-bar"></nav>
  </div>
</template>

<script setup>
import LoginButton from "@/components/buttons/login-button.vue";
import logoutButton from "@/components/buttons/logout-button.vue";
import SignupButton from "@/components/buttons/signup-button.vue";

import { useAuth0 } from "@auth0/auth0-vue";

const { isAuthenticated } = useAuth0();
</script>
