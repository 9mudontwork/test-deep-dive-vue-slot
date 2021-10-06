<template>
  <div>
    <child-a>
      <template #slot-a>
        <div class="asdasd">
          {{ testData.a }}
        </div>
      </template>

      <template #slot-b="{ handleClickChildA }">
        <button
          class="bg-red-500 text-white w-[200px] h-[200px] p-8"
          @click="handleClickChildA()"
        >
          index - call function in child a
        </button>
      </template>

      <template #slot-c="{ buttonName }">
        <button
          class="bg-black text-white w-[200px] h-[200px] p-8"
          @click="handleClick()"
        >
          index - "{{ buttonName.slotC }}"
        </button>
      </template>

      <template #component-a>
        <!-- component a -->
        <component-a>
          <template #button-component-a>
            <button
              class="bg-green-500 text-white w-[200px] h-[200px] p-8"
              @click="handleClick()"
            >
              index - component a
            </button>
          </template>
        </component-a>
      </template>

      <template #button-component-b>
        <button
          class="bg-green-500 text-white w-[200px] h-[200px] p-8"
          @click="handleClick()"
        >
          index - component b
        </button>
      </template>
    </child-a>

    <div class="isIndex">
      <test-slot var-from-index="testData.a">
        <template #test-slot-a></template>
      </test-slot>
    </div>
  </div>
</template>

<script>
import ComponentA from '../components/child-a/ComponentA.vue'
import ChildA from '../components/ChildA.vue'
import TestSlot from '../components/child-a/TestSlot.vue'

export default {
  components: { ChildA, ComponentA, TestSlot },

  data() {
    return {
      testData: {
        a: 'ข้อความจาก Index',
        b: 'prop b asdasdasdasd',
      },
    }
  },

  methods: {
    handleClick() {
      alert('alert from index')
    },
  },
}
</script>
