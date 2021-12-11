<template>
  <div class="home">
  <div>Home Page  {{injectedValue}}</div>
  <Comp/>
  <Header/>
  <Footer/>
  <Injecter/>
  </div>
</template>

<script lang="ts">
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';
import Injecter from '@/components/Injecter.vue';
import { Component, Vue } from 'vue-property-decorator';
import Comp from '@/components/Comp.vue';
 import { Inject } from 'vue-property-decorator';
@Component({
  components: {
   Header,Comp,Footer,Injecter
  },
})
export default class Home extends Vue {
 @Inject('a')  injectedValue!: string;


 mounted():void {
  console.log(this.injectedValue);
 }


}
</script>
