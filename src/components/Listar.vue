<template>
    <div>
        <Encabezado texto="Usuario del sistema" />
    </div>
</template>

<script>
import Encabezado from '@/components/Header.vue'
export default {
    data(){
        return {
            alumnos: [],
        }
    },
    components: {
        Encabezado
    },
    methods: {
        consultarAlumnos(){
            fetch('http://localhost:8888/')
            .then(res => res.json())
            .then( (datos) => {
                this.alumnos = datos
                console.log('alumnos', this.alumnos)
            })
            .catch(console.log)
        }
    },
    created: function(){
        console.log('alumnos antes de ejecucion',this.alumnos)
        this.consultarAlumnos()
    }
}
</script>