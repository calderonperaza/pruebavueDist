<template>
<button @click="lanzarEvento">{{titulo}}</button>
</template>

<script>
export default {
    name: "Botoncuenta",
    props: {
        titulo: {
            type: String,
            default: "Soy un boton"
        }
    },
    methods: {
        lanzarEvento() {
            this.$emit("hicieronclick", 25)
        }
    },
}
</script>

<style scoped>

</style>
