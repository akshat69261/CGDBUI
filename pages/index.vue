<template>
  <main>
    <NuxtLink to="/datatable"> Datatable </NuxtLink>
    <div>{{ content }}</div>
    <button @click="refresh">Refresh</button>
  </main>
</template>
<script>
window.onNuxtReady(() => {});

export default {
  asyncData() {
    return { content: "Created at: " + new Date() };
  },
  methods: {
    refresh() {
      this.$nuxt.refresh();
    },
  },
};
</script>