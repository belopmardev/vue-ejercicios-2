<template>
  <div class="about">
    <h1>Kaio-ken</h1>
    <Mayus />
    <Mayus number="2" hi="Welcome"/>
    <Mayus number="3" hi="Aloha"/>
  </div>
</template>

<script>
import Mayus from '@/components/Mayus.vue'

export default {
  name: 'Kaioken',
  components: {
    Mayus
  }
}
</script>
