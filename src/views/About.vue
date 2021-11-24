<template>
  <div id="table">
    <table>
      <template v-for="row in rows">
        <tr
          @click="toggle(row.id)"
          :class="{ opened: opened.includes(row.id) }"
          v-bind:key="row.id"
        >
          <td>{{ row.name }}</td>
          <td>{{ row.handle }}</td>
        </tr>
      </template>
    </table>
  </div>
</template>




<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
interface IRows {
  id: number;
  name: string;
  handle: string;
}

@Component({
  components: {},
})
export default class Home extends Vue {
  opened: string[] = [];

  rows: Array<IRows> = [
    { id: 1, name: "Bill", handle: "bill" },
    { id: 2, name: "Bob", handle: "bob" },
    { id: 3, name: "Jim", handle: "jim" },
    { id: 4, name: "Leroy", handle: "leroy" },
  ];
  /* eslint-disable */
  toggle(id: any): void {
    const index = this.opened.indexOf(id);
    if (index > -1) {
      this.opened.splice(index, 1);
    } else {
      this.opened.push(id);
    }
  }
}
</script>

<style scoped>
table {
  width: 100%;
  border: 1px solid #ccc;
}

td {
  padding: 2px;
  border: 1px solid #ccc;
}

.opened {
  background-color: yellow;
}
</style>
