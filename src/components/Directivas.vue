<template>
    <div>
        <h1>Directivas Vue</h1>
        <label>Nombre:</label>
        <input type="text" v-model="nombre"/><br/>
        <label> Edad:</label>
        <input type="text" v-model="edad"><br/>
        <h1>
            {{nombre}}, {{edad}}
        </h1>
        <h1>
            {{$data}}
        </h1>
    </div>
</template>

<script>
export default {
    name:"Directivas",
    data() {
        return{
            nombre: "",
            edad: 0
        }
    }
}
</script>

