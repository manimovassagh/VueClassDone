<template>
  <div id="table">
   <h1>check</h1>
   <div >{{fullName()}}</div>
  </div>
</template>




<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {
   
  },
})
export default class Contact extends Vue {
 
 name='mani'
 family='Movassagh'

fullName():string{
   return ` This is a ${this.name} and this is a ${this.family}`
  }
   
}

</script>

<style scoped>

</style>
