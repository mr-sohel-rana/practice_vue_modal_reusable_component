<template>
  <div v-if="show" class=" mx-auto fade w-100 h-100 bg-yellow-200 ">
      <div >
        <h1>{{ title }}</h1>
        <Button type="one" @click="closeModal">X</Button>
    </div>
    <div>
        <slot></slot>
    </div>

    <div>
        <Button type="one" @click="closeModal">close</Button>
          <Button type="two" @click="emit('confirm')">Confirm</Button>
    </div>
  </div>
</template>
<script setup>
import Button from './Button.vue'
const props=defineProps({
    title: { type: String, required: true },
    show:{type:Boolean,required:true}
})
const emit = defineEmits(['close', 'confirm'])
const closeModal = () => {
    emit('close')
}
</script>