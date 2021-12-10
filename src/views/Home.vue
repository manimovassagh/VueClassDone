<template>
  <div class="home">
  <div>Home Page</div>
  <Comp/>
  <Header/>
  </div>
</template>

<script lang="ts">
import Header from '@/components/Header.vue';
import { Component, Vue } from 'vue-property-decorator';
import Comp from '@/components/Comp.vue';

@Component({
  components: {
   Header,Comp
  },
})
export default class Home extends Vue {}
</script>
