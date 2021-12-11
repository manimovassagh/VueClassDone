<template>
  <h1>check {{this.user}} </h1>
</template>

<script lang="ts">
export default {

inject: ['user'],
created() {
    console.log(`Injected property: ${this.user}`) // > Injected property: John Doe
  },
  data() {
    return {
     say: 'mani'
     }
  }

}
</script>

<style>

</style>