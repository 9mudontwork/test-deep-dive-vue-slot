<template>
  <div class="text-center mt-4 space-x-4">
    <slot name="slot-a"></slot>
    <slot name="slot-b" :handleClickChildA="handleClickChildA" />
    <slot name="slot-c" :button-name="buttonName" />
    <br />

    <div class="mt-4">
      child a
      <slot name="component-a"></slot>
    </div>

    <div class="mt-4">
      child a
      <component-b>
        <template #button-component-b>
          <slot name="button-component-b"></slot>
        </template>
      </component-b>
    </div>
  </div>
</template>

<script>
import ComponentB from './child-a/ComponentB.vue'
export default {
  components: { ComponentB },
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
