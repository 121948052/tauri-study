<!--
 * @Author: Bug Router
 * @Date: 2023-09-20 14:16:58
 * @Description: Default
-->
<script setup>
import { open } from '@tauri-apps/api/shell';

async function openFn () {
  // Learn more about Tauri commands at https://tauri.app/v1/guides/features/command
  await open('https://stackoverflow.com/', 'firefox');
}
</script>

<template>
  <form class="row" @submit.prevent="openFn">
    <button type="submit">
      Go stackoverflow
    </button>
  </form>
</template>
