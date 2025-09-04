 <template>
    <div class="w-15 h-6   rounded-full flex items-center transition cursor-pointer"
     :class="modelValue ? 'bg-green-400':'bg-gray-400' "
    >
<div class=" w-5 h-5 bg-white  rounded-full transition transition-duration-300"
:class="modelValue? 'translate-x-9':'translate-x-0'"
@click="toggle"
>

</div>

    </div>

 </template>

 <script setup>
const props = defineProps({
    modelValue:{type:Boolean,default:false}
})
const emit = defineEmits(['update:modelValue'])

const toggle = () => {
    emit("update:modelValue", !props.modelValue)
}

</script>