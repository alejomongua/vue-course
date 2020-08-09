<template>
  <div class="hello">
    <h1>Skills</h1>
    <ul>
      <li v-for='(data, index) in skills' :key='index'>
        {{ index + 1 }} -  {{ data }}
      </li>
    </ul>


    <div v-if='!!alert' class='alert'>{{alert}}</div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data () {
    return {
      skills: [
        'react',
        'vue',
        'ssr',
        'python',
        'javascript',
        'ruby'
      ],
      alert: null,
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
a {
  color: #42b983;
}
.alert {
  background-color: lightpink;
  color: white;
}
</style>
