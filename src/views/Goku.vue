<template>
  <div class="about">
    <h1>Estoy en About</h1>
    <Personaje fuerza="20" />
    <Personaje fuerza="30" />
    <Personaje fuerza="40" />
  </div>
</template>

<script>
import Personaje from '@/components/Personaje.vue'
import Reactividad from '@/components/Reactividad.vue'

export default {
  name: 'About',
  components: {
    Personaje,
    Reactividad
  }
}
</script>
