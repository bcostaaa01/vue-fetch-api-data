<template>
<div>
<button @click="logData">Display data</button>
{{result}}
</div>
</template>

<script>
import {ref} from 'vue'

export default {
  setup () {
    const result = ref(null)

    fetch("https://jsonplaceholder.typicode.com/todos")
    .then(response => response.json())
    .then(data => result.value = data)

    return {result}
  }
}



</script>