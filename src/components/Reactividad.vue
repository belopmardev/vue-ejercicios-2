<template>
    <div>
        <div class="centrar">
            <h2>Este es el componente Mayúsculas nº{{number}}</h2>
            <img src="@/assets/kaioken.png" alt="Kaioken">
            <div class="centrar"><button @click="toUpperCase">Pasar a Mayúsculas</button>
            <h3>{{msg}}</h3></div>
        </div>
    </div>
</template>

<script>

import {ref} from 'vue'
export default {
    name: 'Reactividad',
    props:{
        msg: {
            type: String,
            default:"Hola"
        },
        number:{
            type: String,
            default: "1"
        },
    },
    setup(props){
        let msg = props.msg
        let msgUpperCase = ref(msg)

        function toUpperCase(){
            msgUpperCase.value=msgUpperCase.value.toUpperCase()
        }
        console.log(msgUpperCase.value)
        console.log(msg)

        function toLowerCase(){
            msgUpperCase.value=msgUpperCase.value.toLowerCase()
        }

        return{
            msgUpperCase,
            toUpperCase,
            toLowerCase
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
    width: 0%;
    filter: drop-shadow(20px -10px 10px #ee2370);
}
.centrar{
    margin: 0 auto;
}
</style>