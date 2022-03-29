<script>
export default {
  data() {
    return {
      text: 'Edit me',
      checked: true,
      checkedNames: ['Jack'],
      picked: 'One',
      selected: 'A',
      multiSelected: ['A'],
    }
  },
}
</script>

<template>
  <h2>Text Input</h2>
  <input v-model="text">
  {{ text }}

  <h2>Checkbox</h2>
  <input type="checkbox" v-model="checked" id="checkbox">
  <label for="checkbox">Checked: {{ checked }}</label>

  <h2>Multi Checkbox</h2>
  <input type="checkbox" v-model="checkedNames" id="jack" value="Jack">
  <label for="jack">Jack</label>

  <input type="checkbox" v-model="checkedNames" id="ccyou" value="CCYOU">
  <label for="ccyou">CCYOU</label>

  <input type="checkbox" v-model="checkedNames" id="mike" value="MIKE">
  <label for="mike">MIKE</label>

  <p>Checked names:
  <pre>{{ checkedNames }}</pre>
  </p>

  <h2>Radio</h2>

  <input type="radio" v-model="picked" id="one" value="ONE">
  <label for="one">ONE</label>
  <br>
  <input type="radio" v-model="picked" id="two" value="TWO">
  <label for="two">TWO</label>
  <br>

  <span>Picked: {{ picked }}</span>

  <h2>Select</h2>
  <select v-model="selected">
    <option disabled value="">Please select one</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
    <option>D</option>
    <option>E</option>
  </select>
  <br>
  <span>Selected: {{ selected }}</span>

  <h2>Multi Select</h2>
  <select multiple v-model="multiSelected" style="width: 100px">
    <option>A</option>
    <option>B</option>
    <option>C</option>
    <option>D</option>
    <option>E</option>
  </select>
  <br>
  <span>Multi Selected: {{ multiSelected }}</span>

</template>

<style>


</style>