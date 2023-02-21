<template>
  <div class="container">
    <h1>{{ name }}'s click counter'</h1>
  </div>

  <div class="display">
    <h3> You have clicked {{ clicks }} times. </h3>
  </div>

  <div class="buttons">
    <button @click="increasecounts">Counter</button>
    <button @click="resetclicks">Reset count</button>
    <button @click="toggleVisibility"> Change name </button>
  </div>

  <div class="forms">
    <input v-show="visibility" v-model="name"/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      clicks: 0,
      name: 'Muhammad',
      visibility: true
    }
  },
  methods: {
    increasecounts() {
      this.clicks++;
    },
    toggleVisibility() {
      this.visibility = !this.visibility
    },
    resetclicks() {
      this.clicks = 0
    }
  }
}
</script>

<style scoped>
  .container {
    margin: auto;
    width: 100%
  }

  .buttons {
    display: flex;
    justify-content: center;
    flex-direction: column;
    margin: auto;
    width: 125px;
  }

  button {
    margin: 5px;
    padding: 8px;
  }
  
  .form {
    margin: 20px;
  }
</style>
