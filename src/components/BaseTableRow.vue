<template>
  <div class="row">
    <slot
      v-for="(jails) in row"
      name="row"
      :jails="jails"
    ></slot>
  </div>
</template>

<script>
export default {
  name: "BaseTableRow",
  props: {
    row: {
      type: Array,
    }
  }
}
</script>

<style lang="scss" scoped>
</style>