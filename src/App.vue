 <template>
  

  <test :studentDetails="studentDetails" type="best"/>

 <Button type="three" @click="showModal=true"  >show modal</Button>

 <Modal1 
  :show="showModal"
 title="student tile"
 @close="showModal=false"
 @confirm="handleConfirm"
 >
 <p>Lorem ipsum dolor sit amet.
 </p>

 </Modal1>
  
</template>

<script setup>
 import Modal1 from './assets/components/Modal1.vue';
import test from './assets/components/Text.vue'
import Button from './assets/components/Button.vue';
import { ref } from 'vue';
const studentDetails = ({
  name: "sohel",
  dept: 'ice',                                                                                                                                                                                                                                                                                                                   
  roll: 8
})
const showModal = ref(false)

const handleConfirm = () => {
  showModal.value = false;
}
                                 
</script>
