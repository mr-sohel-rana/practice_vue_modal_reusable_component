 <template>
  

  <test :studentDetails="studentDetails" type="best"/>

 <Button type="three"  >sohel</Button>
  
</template>

<script setup>
 
import test from './assets/components/Text.vue'
import Button from './assets/components/Button.vue';
const studentDetails = ({
  name: "sohel",
  dept: 'ice',                                                                                                                                                                                                                                                                                                                   
  roll: 8
})
                                 
</script>
