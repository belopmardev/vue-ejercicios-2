<template>
    <div>
        <img src="@/assets/goku.png" alt="Goku">
        <div class="contador"><h3>Fuerza Actual:{{fuerzaActual}}</h3></div>
        <button class="cabrear" @click="cabrear">Cabrear a Goku</button>
        <button class="calmar" @click="calmar">Calmar a Goku</button>
    </div>
</template>

<script>
import {ref} from 'vue'

export default {
  name: 'Personaje',
  props: {
      fuerza:{
        type: String,
        default: "0",
        required: true
      }
  },
  setup(props){
    let fuerzaActual=ref(props.fuerza)

    const cabrear=()=>{
        fuerzaActual.value++
    }

    const calmar=()=>{
        fuerzaActual.value--
    }
    
    return {
        fuerzaActual,
        cabrear,
        calmar
    }
  }
}
</script>
<style lang="scss" scoped>
button{
    border: none;
    border-radius: 50%;
    color: #fff;
    width: 150px;
    height: 50px;
    margin: 1rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 1rem;
    box-shadow: 0px 5px 1px grey;
    &.cabrear{
        background: rgb(116, 14, 14);
    }
    &.calmar{
        background: #42b983;
    }
}

button:hover{
    background: grey;
}

img {
    width: 15%;
    filter: drop-shadow(10px 0px 5px black);
}

.contador{
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    height: 50px;
    width: 150px;

}
</style>