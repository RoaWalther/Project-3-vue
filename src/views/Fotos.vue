<template>
    <div>
        <h1>Galeria de imagenes</h1>
        <router-link :to="{name:'Fotos', params: {id: item}}" 
        v-for="(item,index) of fotos" :key="index">
            <button>Foto: {{item}}</button>
        </router-link>
        <Foto></Foto>
        <button @click="about">Aboutodo</button>
    </div>
</template>

<script>
import Foto from '@/components/Fotografia.vue'
export default {
    name: 'Fotos',
    components: {
        Foto
    },
    data() {
        return {
            fotos:[1,2,3]
        };
    },
    methods: {
        about(){
            this.$router.push('/about')
        }
    },
}
</script>
