<template>
  <div
    class="badge"
    :style="{
      ...badgeOptions
    }"
  >
  </div>
</template>

<script>
export default {
  name: "BaseBadge",
  props: {
    badgeOptions: Object,
    status: String
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
  width: 1rem;
  height: 1rem;
  min-width: 1rem;
  min-height: 1rem;
  max-width: 1rem;
  max-height: 1rem;
}
</style>