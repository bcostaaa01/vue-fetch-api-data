<template>
<div>
<h1>Data from JSON Placeholder API</h1>
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