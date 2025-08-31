 <template>
  <div
    v-if="show"
    class="fixed inset-0 flex items-center justify-center bg-black/50 z-50"
  >
    <div class="bg-white rounded-lg shadow-lg w-96 p-4 relative">
      <!-- Header -->
      <div class="flex justify-between items-center border-b pb-2 mb-2">
        <h2 class="text-lg font-semibold">{{ title }}</h2>
        <button @click="closeModal" class="text-gray-500 hover:text-black">✖</button>
      </div>

      <!-- Content slot -->
      <div class="mb-4">
        <slot />
      </div>

      <!-- Footer with actions -->
      <div class="flex justify-end gap-2 border-t pt-2">
        <Button type="one" @click="closeModal">Close</Button>
        <Button type="two" @click="$emit('confirm')">Confirm</Button>
      </div>
    </div>
  </div>
</template>

<script setup>
import Button from "./Button.vue";

defineProps({
  show: { type: Boolean, required: true },
  title: { type: String, default: "Modal Title" }
});

const emit = defineEmits(["close", "confirm"]);

const closeModal = () => {
  emit("close");
};
</script>
