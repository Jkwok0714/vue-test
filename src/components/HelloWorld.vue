<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Members of Vue Party</h2>
    <ul>
      <li v-for="member in members" :key="member.name">
        {{ member.name }}, the {{ member.class }}
      </li>
    </ul>
    <input type="text" v-model="inputVal" @change="counter++">
    <div>
      Input: <span v-text="inputVal"></span> was changed <span v-text="counter"></span> times
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      members: [{
        name: 'Serenna', class: 'Priest',
      },
      {
        name: 'Valin', class: 'Swordman',
      },
      {
        name: 'Armadus', class: 'Paladin',
      },
      {
        name: 'Ashera', class: 'Assassin',
      }],
      inputVal: '',
      counter: 0,
    };
  },
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
</style>
