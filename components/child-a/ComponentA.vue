<template>
  <div>
    <p>component a</p>
    <slot name="button-component-a"></slot>
    <div class="mt-4">
      <button
        class="bg-green-500 text-white w-[200px] h-[200px] p-8"
        @click="handleClick()"
      >
        component a
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },

  methods: {
    handleClick() {
      alert('alert from copmponent a')
    },
  },
}
</script>
