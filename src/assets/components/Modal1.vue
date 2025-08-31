<template>
  <div v-if="show">
      <div >
        <h1>{{ title }}</h1>
        <button @click="closeModal">X</button>
    </div>
    <div>
        <slot></slot>
    </div>

    <div>
        <button @click="closeModal">close</button>
          <button @click="emit('confirm')">Confirm</button>
    </div>
  </div>
</template>
<script setup>
const props=defineProps({
    title: { type: String, required: true },
    show:{type:Boolean,required:true}
})
const emit = defineEmits(['close', 'confirm'])
const closeModal = () => {
    emit('close')
}
</script>