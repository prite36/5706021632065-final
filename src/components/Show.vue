<template lang="html">
  <div class="">
    <table class="table">
      <tbody>
        <tr>
            <td width="400">{{list.name}}</td>
            <td width="400">{{list.credit}}</td>
            <td width="400">{{list.grade}}</td>
            <td width="400"><button class="button is-danger" type="button" name="button" @click="deletelist(list.id)">X</button></td>
        </tr>
      </tbody>
</table>
  </div>
</template>

<script>
export default {
  props: ['list', 'deletelist'],
  data () {
    return {
      edit: false,
      name: this.list.name,
      credit: this.list.credit
    }
  },
  methods: {
    editData () {
      this.editList(this.list.id, this.name, this.surname)
      this.edit = false
    }
  }
}
</script>

<style lang="css">
</style>
