<script setup></script>

<template>
  <div>
    <header>
      <Topnav />
      <Sidebar />
    </header>
    <main>
      <div class="pl-6 pr-5 pt-24 lg:ml-64">
        <slot />
      </div>
    </main>
  </div>
</template>

<style>
body {
  background-color: #f4f4f4;
}
</style>
