 <template>
  

  <!-- <test :studentDetails="studentDetails" type="best"/> -->

 <!-- <Button type="three" @click="showModal=true"  >show modal</Button> -->
<!-- 
 <Modal1 
  :show="showModal"
 title="student tile"
 @close="showModal=false"
 @confirm="handleConfirm"
 >
 <p>Lorem ipsum dolor sit amet.
 </p>

 </Modal1> -->
 <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum doloribus iusto 
  explicabo culpa sapiente voluptas delectus in repellendus! Aliquid, dolore?</p>

 <Button type="three" @click="DrayerShow=true"  >show modal</Button>
 <DrayerModal
 :show="DrayerShow"
 title="Drayer modal"
 @close="DrayerShow=false"
 >

 </DrayerModal>
  
   <Switch v-model="status" />
  
</template>

<script setup>
import Switch from './assets/components/Switch.vue';
//  import Modal1 from './assets/components/Modal1.vue';
 import DrayerModal from './assets/components/DrayerModal.vue';
// import test from './assets/components/Text.vue'
import Button from './assets/components/Button.vue';
import { ref } from 'vue';
// const studentDetails = ({
//   name: "sohel",
//   dept: 'ice',                                                                                                                                                                                                                                                                                                                   
//   roll: 8
// })
// const showModal = ref(false)

// const handleConfirm = () => {
//   showModal.value = false;
// }

const DrayerShow = ref(false)
const status=ref(false)

                                 
</script>
