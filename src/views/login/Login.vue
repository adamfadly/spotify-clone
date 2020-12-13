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
        <button
          @click.prevent="redirectLogin()"
          id="button-login"
          class="text-white text-xl bg-green p-5 rounded focus:outline-none"
        >
          Login With Spotify
        </button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Login extends Vue {
  redirectLogin(): string {
    const clientId = process.env.VUE_APP_SPOTIFY_CLIENT_ID;
    const urlRedirect = `https://accounts.spotify.com/authorize?${clientId}&response_type=token&redirect_uri=http%3A%2F%2Flocalhost%3A8080%2F&scope=user-read-private%20user-read-email&state=34fFs29kd09`;
    console.log(process.env);
    return (window.location.href = urlRedirect);
  }
}
</script>
