<template>
  <div id="app">
    <div class="main ui container">
      <h2 class="ui dividing header">Semantic Elements:<a class="anchor" id="types"></a></h2>

        <accordion></accordion>

        <semantic-example title="Form Dropdown" :exampleCode="formDropdownCode">
          <semantic-form-dropdown placeholder="Placeholder text" :options="options" :value="someValue" class="example"></semantic-form-dropdown>
        </semantic-example>

        <semantic-example title="Dropdown with freetext search" :exampleCode="formDropdownCode">
          <semantic-dropdown class="example" full-text-search="true">
            <div class="item">one</div>
            <div class="item">two</div>
            <div class="item">three</div>
          </semantic-dropdown>
        </semantic-example>

    </div>
  </div>
</template>

<script>
import Accordion from './components/Accordion';

export default {
  name: 'app',
  components: {
    Accordion,
  },
  data() {
    return {
      options: [
        { id: 1, name: 'one' },
        { id: 2, name: 'two' },
        { id: 3, name: 'three' },
      ],
      someValue: 1,
      formDropdownCode: '<semantic-form-dropdown placeholder="Placeholder text" :options="options" :value="someValue"></semantic-form-dropdown>',
    };
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
