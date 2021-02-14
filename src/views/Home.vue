<template>
  <div class="home">
    <h1>Estoy en la Home</h1>
    <Personaje fuerza=10 />
    <Mayus />
  </div>
</template>

<script>
import Personaje from '@/components/Personaje.vue'
import Mayus from '@/components/Mayus.vue'

export default {
  name: 'Home',
  components: {
    Personaje,
    Mayus
  }
}
</script>

<style scoped lang="scss">
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
</style>