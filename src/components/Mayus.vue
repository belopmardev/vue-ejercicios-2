<template>
    <div>
        <div class="centrar">
            <h2>{{hi}}. Este es el componente de reactividad nº{{number}}</h2>
            <img src="@/assets/kaioken.png" alt="Kaioken">
            <h3>{{msgUpperCase}}</h3>
            <button @click="pasarAMinusculas">Pasar a Minúsculas</button>
        </div>
    </div>
</template>

<script>
import {ref} from 'vue'
export default {
    name: 'Mayus',
    props:{
        number:{
            Type: String,
            default: "1"
        },
        hi:{
            Type: String,
            default: "Hola"
        }
    },
    setup(){
        let msg = "Bienvenido"
        let msgUpperCase = ref(pasarAMayusculas(msg))

        function pasarAMayusculas(){
            return msg.toUpperCase()
    
        }

        function pasarAMinusculas(){
            msgUpperCase.value=msgUpperCase.value.toLowerCase()
        }

        return{
            msgUpperCase,
            pasarAMinusculas
        }
    }
}
</script>

<style lang="scss" scoped>
button{
    border: none;
    border-radius: 50%;
    color: #fff;
    background: #ee2370;
    width: 150px;
    height: 50px;
    margin: 1rem;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 1rem;
    float: center;
}
button:hover{
    background: #0c5a6f;
    box-shadow: 0 12px 16px 0 rgba(0,0,0,0.7), 0 17px 50px 0 rgba(0,0,0,0.7);
}
img{
    width: 20%;
    filter: drop-shadow(20px -10px 10px #ee2370);
}
.centrar{
    margin: 0 auto;
}
</style>