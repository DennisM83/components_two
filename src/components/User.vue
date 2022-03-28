<template>
  <p>The user is {{ age }} years old</p>
  <button type="button" @click="onClickAge">Update Age</button>
</template>

<script>
export default {
  name: 'newUser',
  props: [
    "age"
  ],
  methods: {
    onClickAge() {
      this.$emit('age-change')
    }
  }
}
</script>
