<template>
  <div>
    <slot name="test-slot-a">
      <div>from test slot a</div>
      <div>{{ varFromIndex }}</div>
    </slot>
  </div>
</template>

<script>
export default {
  props: { varFromIndex: String },
}
</script>
