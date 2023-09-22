<!--
 * @Author: Bug Router
 * @Date: 2023-09-22 17:30:55
 * @Description: Default
-->
<script setup>
import { isPermissionGranted, requestPermission, sendNotification } from '@tauri-apps/api/notification';

async function openFn () {
  let permissionGranted = await isPermissionGranted();
  if (!permissionGranted) {
    const permission = await requestPermission();
    permissionGranted = permission === 'granted';
  }
  if (permissionGranted) {
    sendNotification('Tauri is awesome!');
    sendNotification({ title: 'TAURI', body: 'Tauri is awesome!' });
  }
}
</script>

<template>
  <form class="row" @submit.prevent="openFn">
    <button type="submit">
      sendNotification
    </button>
  </form>
</template>
