<template lang="html">
  <div class="">
    <table class="table">
  <thead>
    <tr>
      <th><abbr title="Name">Name</abbr></th>
      <th><abbr title="Credit">Credit</abbr></th>
      <th><abbr title="Greade">Greade</abbr></th>
      <th><abbr title="Delete">Delete</abbr></th>
    </tr>
  </thead>
  </table>
   <show v-for = " list in lists" :list="list" :deletelist="deletelist"></show>
  </div>
</template>
<script>
import show from './show'
export default {
  props: ['lists', 'deletelist'],
  components: {
    show
  }
}
</script>
<style lang="css">
</style>
