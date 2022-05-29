<template>
  <div
    class="jail"
    :class="{
      elipsis
    }"
  >
    <slot
      v-for="jail in jails"
      :jail="jail"
      :name="keyName"
    ></slot>
  </div>
</template>

<script>
export default {
  name: "BaseRowJails",
  props: {
    jails: Object,
    elipsis: {
      type: Boolean,
      default: false
    },
  },
  computed: {
    keyName() {
      return Object.keys(this.jails)[0]
    }
  }
}
</script>

<style lang="scss">
.jail {
  flex: 1 0 auto;
  justify-content: flex-start;
  display: flex;
}
</style>