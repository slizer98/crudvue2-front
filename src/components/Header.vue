<template>
    <div class="text-center">
        <span class="text-h6">
        Proyecto vue 3 + vuetify + php + Mysql
        </span>
        <br>
        <span class="text-subtitle-1-md">
            {{ texto }}
        </span>
    </div>
</template>

<script>
export default {
    props:{
        texto: String
    }
}
</script>