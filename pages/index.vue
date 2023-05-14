<template>
  <div>
<Person :name="personSzymon.name" :student="true" />
 </div>
</template>

<script>
import Customer from '../components/models/customer'
import Person from '../components/person/person.vue'
export default {
  name: 'IndexPage',
  components: { Person },

  date(){
    return {
      personSzymon: null
    }
  },
  
  created() {
      this.personSzymon = this.person('Szymon', '1213241', '18')

  },


  methods: {
    person(imie, salary, age) {
      return new Customer(imie, salary, age);
      
    }
  }
}
</script>
<style scoped>
@import '@/assets/css/index.css';
</style>
