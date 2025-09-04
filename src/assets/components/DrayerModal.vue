 <template>
  <transition name="slide">
    <div
      v-if="show"
      class="fixed top-0 right-0 w-80 h-full bg-white shadow-xl z-50"
    >
      <div class="flex justify-between items-center p-4 bg-blue-500 text-white">
        <h2 class="text-lg font-semibold">{{ title }}</h2>
        <button @click="$emit('close')">X</button>
      </div>
      <div class="p-4">
        <h2 class=" ">Name : SOHEL RANA</h2>
        <hr class="w-auto m-4  ">
        <slot />
      </div>
    </div>
  </transition>
</template>

<script setup>
const props = defineProps({
  title: String,
  show: Boolean
})
</script>
<style>
.slide-enter-active,
.slide-leave-active { transition: transform 0.3s ease; }
.slide-enter-from { transform: translateX(100%); }
.slide-enter-to { transform: translateX(0); }
.slide-leave-from { transform: translateX(0); }
.slide-leave-to { transform: translateX(100%); }
</style>

