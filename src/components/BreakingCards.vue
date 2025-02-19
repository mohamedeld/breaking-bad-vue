<script setup>
import { onMounted } from 'vue'
import axios from 'axios'
import { reactive } from 'vue'

const state = reactive({
  characters: [],
  isLoading: true,
})

onMounted(async () => {
  try {
    const response = await axios.get(`https://jsonplaceholder.typicode.com/photos`)

    if (response?.status === 200) {
      state.characters = response?.data
    }
  } catch (error) {
    console.log(error)
  } finally {
    state.isLoading = false
  }
})
</script>

<template>
  <div></div>
</template>
