<script >
import data from './../assets/datos.json'
import Suma from './CirculoPastel.vue'

export default{
    data(){
        return{
            lista:data
        }
    }
}


</script>


<template>
    <div class="max-w-md overflow-hidden shadow-lg" name="form1">
        <div class="px-6 py-4 text-white text-xl bg-gradient-to-r from-indigo-500 to-purple-500 rounded-3xl ">
            <h2 class="font-bold text-2xl mb-2">Avance</h2>
        <div v-for="item in lista.Proyecto.Partes" > 
        <ul>
        <li><input type="checkbox"> {{ item.Titulo }}</li>
        <li>{{ item.Descripcion }}</li>
        <li></li>
        </ul>
    
        </div>
    </div>
    </div>
    
    


</template>