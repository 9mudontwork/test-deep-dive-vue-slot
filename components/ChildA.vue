<template>
  <div class="text-center mt-4 space-x-4">
    <slot name="slot-a"> </slot>
    <slot name="slot-b" :handleClickChildA="handleClickChildA" />
    <slot name="slot-c" :button-name="buttonName" />
    <br />

    <div class="mt-4">
      child a
      <slot name="component-a"></slot>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      buttonName: {
        slotC: 'child a',
      },
    }
  },
  methods: {
    handleClickChildA() {
      alert('alert from child a')
    },
  },
}
</script>
