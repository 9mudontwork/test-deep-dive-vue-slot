<template>
  <div>
    <p>component b</p>
    <slot name="button-component-b"></slot>
    <div class="mt-4">
      <button
        class="bg-green-500 text-white w-[200px] h-[200px] p-8"
        @click="handleClick()"
      >
        component b
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
      alert('alert from copmponent b')
    },
  },
}
</script>
