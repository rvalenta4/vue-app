<template>

  <ul>
    <h1>A list of persons</h1>
    <li v-for="person in persons" v-bind:key="person.id">
      {{ person.name }}
    </li>
  </ul>
  
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    },
    data: () => {
      return {
        persons: [
          {id: 0, name: 'John', dead: false},
          {id: 1, name: 'Mary', dead: true},
          {id: 2, name: 'Peter', dead: false},
          {id: 3, name: 'Caroline', dead: false},
          {id: 4, name: 'Josh', dead: false},
        ]
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  .test {
    color: red;
  }
</style>
