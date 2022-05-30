<template>
  <div
    class="badge"
    :style="{
      ...badgeOptions,
      backgroundColor: colors[status]
    }"
  >
  </div>
</template>

<script>
export default {
  name: "BaseBadge",
  props: {
    badgeOptions: Object,
    status: String,
    colors: Object
  },
  data() {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
</style>