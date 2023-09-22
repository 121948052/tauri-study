<!--
 * @Author: Bug Router
 * @Date: 2023-09-20 14:16:58
 * @Description: Default
-->
<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Greet from "./components/Greet.vue";
import Open from "./components/TauriApi/Open.vue";
import OS from "./components/TauriApi/OS.vue";
import Notification from "./components/TauriApi/Notification.vue";

</script>

<template>
  <div class="container">
    <h1>Welcome to Tauri!</h1>

    <div class="row">
      <a
        href="https://tauri.app"
        target="_blank"
      >
        <img
          src="/tauri.svg"
          class="logo tauri"
          alt="Tauri logo"
        />
      </a>
    </div>

    <p>
      Click on the Tauri, Vite, and Vue logos
      to learn more.
    </p>

    <p>
      Recommended IDE setup:
      <a
        href="https://code.visualstudio.com/"
        target="_blank"
        >VS Code</a
      >
      +
      <a
        href="https://github.com/johnsoncodehk/volar"
        target="_blank"
        >Volar</a
      >
      +
      <a
        href="https://github.com/tauri-apps/tauri-vscode"
        target="_blank"
        >Tauri</a
      >
      +
      <a
        href="https://github.com/rust-lang/rust-analyzer"
        target="_blank"
        >rust-analyzer</a
      >
    </p>

    <Greet />
    <Open />
    <OS />
    <Notification />
  </div>
</template>

<style scoped>
.logo.vite:hover {
  filter: drop-shadow(0 0 2em #747bff);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #249b73);
}
</style>
