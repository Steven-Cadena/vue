<template>
    <div>
        <h1>Propiedades conmutadas</h1>
        <ul>
            <li v-for="juego in juegos" :key="juego">
                {{juego | mayusculas}}
                {{juego | mayusculasParametro("Juegazoo")}}
            </li>
        </ul>
        <hr/>
        <ul>
            <li v-for="j in juegosRojos" :key="j" v-html="j">
                {{j}}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:"JuegosConmutados",
    filters: {
        mayusculas(dato){
            return dato.toUpperCase();
        },
        mayusculasParametro(dato,restriccion){
            return dato.toUpperCase() + restriccion;
        }
    },
    computed: {
        //UNA PROPIEDAD CONMUTADA SIEMPRE DEVULVE UN VALOR Y NO TIENE PARAMETROS 
        juegosRojos(){
            var datos = this.juegos;
            for ( var i = 0; i<datos.length; i++){
                var juego = datos[i];
                juego = "<span style='color:red'>"
                + juego + "</span>";
                datos[i] = juego;
            }
            return datos;
        }
    },
    data() {
        return{
            juegos:["Canicas","Petanca","Parchis","La cuerda","Las galletas"]
        }
    }
}
</script>