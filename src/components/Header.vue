<template>
  <div class="home">
  <div>{{name}}</div>
  </div>
</template>

<script lang="ts">

import { Component, Provide, Vue } from 'vue-property-decorator';


@Component({
  components: {
   
  },
})
export default class Header extends Vue {
  name="mani"
  @Provide  ('a')  providedValue = 'The value';

  // eslint-disable-next-line @typescript-eslint/explicit-module-boundary-types
  mounted() {
    console.log(this.providedValue);
  }
}
</script>

