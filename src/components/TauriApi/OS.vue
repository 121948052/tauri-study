<!--
 * @Author: Bug Router
 * @Date: 2023-09-22 17:30:55
 * @Description: Default
-->
<script setup>
import { ref } from "vue";
import { type, version } from '@tauri-apps/api/os';

const osType = ref("");
const osVersion = ref("");

async function openFn () {
  osType.value = await type();
  osVersion.value = await version();

}
</script>

<template>
  <form class="row" @submit.prevent="openFn">
    <button type="submit">os infos</button>
  </form>
  <p>{{ osType }}</p>
  <p>{{ osVersion }}</p>
</template>
