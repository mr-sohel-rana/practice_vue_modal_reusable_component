 <template>
  <h1 class="w-25 p-6 m-5"
    :class="{
    'bg-blue-500 text-white p-2 rounded':
        type === 'good',
    'bg-green-500 text-white p-2 rounded':
        type === 'bad',
    'bg-yellow-500 text-black p-2 rounded':
        type === 'best',
    'bg-gray-400 text-white p-2 rounded':
        type === 'average',
    'bg-red-500 text-white p-2 rounded':
        type === 'poor',
    }"
  >
    {{ studentDetails.name }}
  </h1>
</template>

<script setup>
const props = defineProps({
  studentDetails: {type:Object},
  type: {type:String}
})
</script>
