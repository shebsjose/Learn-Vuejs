<template>
 <div class="home">
    <h1>Home</h1>
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>
    <button @click="age++">add 1 to age</button>
    <input type="text" v-model="name">
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Home',
  setup() {
    //let name = 'mario'
    //let age = 30
    //const p = ref(null)
     const name = ref('mario')
    const age = ref(30)
    // const handleClick = (e) => {
    //   console.log(p, p.value)
    //   p.value.classList.add('test')
    //   p.value.textContent = 'hello, ninjas'
    // }
     const handleClick = (e) => {
      name.value = 'luigi'
      age.value = 35
     }
    // console.log(p.value)
    return { name, age, handleClick,  }
  },
}
</script>