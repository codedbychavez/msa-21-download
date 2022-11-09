<template>
  <section>
    <div class="container">
      <Downloads />
    </div>
  </section>
</template>

<script>
import Downloads from "@/components/Downloads/Downloads.vue";

export default {
  components: {
    Downloads,
  },
};
</script>

<style lang="scss">
.container {
  padding: 24px;
}

@media (min-width: 700px) {
  .container {
    padding: 64px;
  }
}
</style>
