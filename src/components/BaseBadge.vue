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
.badge {
  display: block;
  width: 1.2rem;
  height: 1.2rem;
  min-width: 1.2rem;
  min-height: 1.2rem;
  max-width: 1.2rem;
  max-height: 1.2rem;
  border-radius: 1.2rem;
}
</style>