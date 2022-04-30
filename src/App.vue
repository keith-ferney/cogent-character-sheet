<script setup lang="ts">
import { RouterView } from "vue-router";</script>

<template>
  <div class=" h-full grid grid-rows-[auto_1fr_auto]">

    <header class="bg-gray-300 p-3">
      <h1>Cogent Roleplay V:1.3.0 Character Sheet</h1>
    </header>

    <main class="p-3">
      <RouterView />
    </main>

    <footer class="bg-gray-300 px-3 py-1">
      Footer
    </footer>
  </div>
</template>
