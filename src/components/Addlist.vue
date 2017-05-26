<template lang="html">
<div class="">
  <div class="columns">
  <div class="column is-half">
    <input class="input is-half" type="text"  v-model="name" placeholder="ชื่อวิชา">
  </div>
  <div class="column ">
    <div class="field">
      <p class="control">
        <span class="select" >
          <select v-model="credit">
            <option>1</option>
            <option>3</option>
          </select>
        </span>
      </p>
    </div>
  </div>
  <div class="column ">
    <div class="field">
      <p class="control">
        <span class="select" >
          <select v-model="grade">
            <option>A</option>
            <option>B+</option>
            <option>B</option>
            <option>C+</option>
            <option>C</option>
            <option>D+</option>
            <option>D</option>
            <option>F</option>
          </select>
        </span>
      </p>
    </div>
  </div>
  <div class="column is-one-quarter">
    <a class="button is-success" @click="addTo">Add Subject</a>
  </div>
</div>




</div>
</template>

<script>
export default {
  props: ['add'],
  data () {
    return {
      name: '',
      cerdit: '',
      grade: ''
    }
  },
  methods: {
    addTo () {
      this.add(this.name, this.credit, this.grade)
      this.name = ''
      this.credit = ''
      this.grade = ''
    }
  }
}
</script>

<style lang="css">
</style>
