<template>
<div>
    <nav>
        <ul id="menu">
            <li>
                <router-link to="/home">Home</router-link>
            </li>
            <li>
                <router-link to="/directivas">Directivas</router-link>
            </li>
            <li>
                <router-link to="/juegosconmutados">Juegos conmutados</router-link>
            </li>
            <li>
                <router-link to="/ciclovida">Ciclo Vida</router-link>
            </li>
            <li>
                <router-link to="/cine">Cine</router-link>
            </li>
            <li>
                <router-link to="/musica">Música</router-link>
            </li>
            <li>
                <router-link to="/television">Televisión</router-link>
            </li>
        </ul>
    </nav>
</div>
    
</template>

<script>
export default {
    name:"Menu",
}
</script>

<style scoped>
ul#menu li{
    display: inline;
    padding: 10px;
}
</style>