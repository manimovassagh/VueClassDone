<template>
  <div class="home">
  <div>{{name}}</div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {
   
  },
})
export default class Header extends Vue {
  name="mani"
}
</script>

