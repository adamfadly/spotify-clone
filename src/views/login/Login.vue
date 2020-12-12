<template>
  <div
    id="login"
    class="bg-dark w-screen h-screen flex flex-row items-center justify-center"
  >
    <div class="items-center justify-center">
      <div class="mb-6 w-96">
        <img src="@/assets/logos-spotify/Spotify_Logo_Green.png" alt="" />
      </div>
      <div class="flex flex-row justify-center">
        <a href="#">
          <button
            @click="redirectLogin()"
            id="button-login"
            class="text-white text-xl bg-green p-5 rounded focus:outline-none"
          >
            Login With Spotify
          </button>
        </a>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Login extends Vue {
  name = 'Login';

  redirectLogin(): string {
    console.log('test');
    return 'test';
  }
}
</script>
