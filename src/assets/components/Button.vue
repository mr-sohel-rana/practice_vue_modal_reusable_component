 <template>
  <button
     
    :class="{
      'bg-red-300 p-2 border border-dotted': type==='one',
      'bg-amber-300 p-2 border border-dotted': type==='two',
      'bg-blue-800 p-2 border text-white border-dotted': type==='three',
    '  p-2  border border-dotted': type === 'four',

    'text-sm py-1 px-2': size === 'sm',
    'text-2xl p-2 m-2 ':size==='lg'
    }"
  >
   
    <slot /> 
  </button>
</template>

<script setup>
const props = defineProps({
  type: { type: String },
  size: { type: String }
})
</script>
