<!--
 * @Author: Bug Router
 * @Date: 2023-09-20 14:16:58
 * @Description: Default
-->
<script setup>
import { ref } from "vue";
import { invoke } from "@tauri-apps/api/tauri";
import { availableMonitors } from '@tauri-apps/api/window';

const greetMsg = ref("");
const name = ref("");

async function greet () {
  debugger
  // Learn more about Tauri commands at https://tauri.app/v1/guides/features/command
  greetMsg.value = await invoke("greet", { name: name.value });
  const monitors = await availableMonitors();
}
</script>

<template>
  <form class="row" @submit.prevent="greet">
    <input
      id="greet-input"
      v-model="name"
      placeholder="Enter a name..."
    />
    <button type="submit">Greet</button>
  </form>

  <p>{{ greetMsg }}</p>
</template>
