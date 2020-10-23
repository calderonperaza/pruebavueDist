<template>
<div>
    <h1>Mi cuenta de ahorros</h1>
    <h2> $ {{ ahorro}}</h2>
    <h3>Gastos de la semana</h3>
    <p v-for="(item,index) in gastos" :key="index">
        {{ item }}
    </p>
    <Botoncuenta titulo="Disminuir" @hicieronclick="DisminuirAhorro" :disabled="ahorro===0" />
    <Botoncuenta titulo="Aumentar" @hicieronclick="AumentarAhorro" />

</div>
</template>

<script>
import Botoncuenta from "./Botoncuenta"

export default {
    name: "Cuenta",
    components: {
        Botoncuenta
    },
    data() {
        return {
            ahorro: 100,
            gastos: ["comprar comida", "libros", "Electricidad", "agua"]
        }
    },
    methods: {
        AumentarAhorro(valor) {
            this.ahorro += valor;
        },
        DisminuirAhorro(valor) {
            this.ahorro -= valor;
        }
    }

}
</script>

<style scoped>

</style>
