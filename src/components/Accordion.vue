<template>
  <div>
    <semantic-example title="Accordion" :exampleCode="accordionCode">
    <semantic-checkbox type="toggle" label="Styled" v-model="styled"></semantic-checkbox>
    <semantic-checkbox type="toggle" label="Fluid" v-model="fluid"></semantic-checkbox>
    <semantic-accordion :styled="styled" :fluid="fluid" :items="accordionItems" class="example"></semantic-accordion>
    </semantic-example>
  </div>
</template>

<script>
export default {
  data() {
    return {
      accordionItems: [
        { title: 'What is a dog', content: 'A dog is a type of domesticated animal. Known for its loyalty and faithfulness, it can be found as a welcome guest in many households across the world.' },
        { title: 'two', content: 'test two' },
      ],
      styled: true,
      fluid: true,
    };
  },
  computed: {
    accordionCode() {
      return `<semantic-accordion :items="accordionItems" ${this.fluid ? '' : ':fluid="false"'} ${!this.styled ? ':styled="false"' : ''}></semantic-accordion>`;
    },
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
