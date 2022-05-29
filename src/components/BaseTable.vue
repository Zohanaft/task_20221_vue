<template>
  <div class="table">
    <slot
      v-for="row in rows"
      :row="row"
      :index="row.index"
      name="rows"
    ></slot>
  </div>
</template>

<script>
export default {
  name: "BaseTable",
  props: {
    rows: {
      type: Array,
    }
  }
}
</script>

<style lang="scss" scoped>
.table {
  display: flex;
  flex-direction: column;
}
</style>