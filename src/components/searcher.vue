<script>
export default {
  data() {
    return { inputSearch: '' };
  },
  watch: {
    inputSearch(event) {
      this.checkContent(event);
    },
  },
  methods: {
    checkContent(event) {
      this.$emit('emitInput', event);
    },
  },
};
</script>
<!-- CAJITA PARA BUSCAR TAREAS-->
<template>
  <div class="d-flex justify-content-end" id="search-filter">
    <input
      class="form-control rounded  text-center border-info"
      type="search"
      v-model="inputSearch"
      placeholder="Search"
    />
    <!-- <span> -->
    <font-awesome-icon class="icon" icon="fa-solid fa-magnifying-glass" />
    <!-- </span> -->
  </div>
</template>
<style>
.icon {
  position: relative;
  right: 30px;
  top: 10px;
}
</style>
