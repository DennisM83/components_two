<template>
  <p>Hey!</p>
  <newGreeting :age="age"/>
  <newUser :age="age" @age-change="updateAge"/>
</template>

<script>
import newGreeting from "./components/Greeting.vue";
import newUser from './components/User.vue';
export default {
  name: 'App',
  components: {
    newGreeting,
    newUser
  },
  data() {
    return {
      age: 20
    }
  },
  methods: {
    updateAge(num) {
     this.age += num
    }
  }

};
</script>
