<template>
    <div class='screen'>
        <!--Formulario parte izquierda-->
        <h1>probando screen</h1>
        <div class='form'>
            <h2 class="form_tittle"><strong>Registro</strong></h2>
                <input class="caja" type="text" v-model="nombre_mascota" placeholder="Nombre de mascota">                    <input class="caja" type="text" v-model="nombre_propietario" placeholder="Nombre propietario">
                <input class="caja" type="text" v-model="telefono" placeholder="Telefono">
                <input class="caja" v-model="fecha" type="date">
                <input class="caja" v-model="tiempo" type="time">
                <textarea class="caja" rows="5" v-model="dolencias" placeholder="Escribe las dolencias del animal"></textarea>
                <input class="boton" @click='Enviar()' type="button" value="Enviar">
        </div>
        <!--Citas parte derecha-->
        <div class='view'>
            <h1>probando view</h1>
        </div>
    </div>
</template>

<script>
export default {
    
    data:{
        nombre_mascota = '',
        telefono = '',
        fecha = '',
        tiempo = '',
        dolencias = ''
    },

    methods:{

    return:{
        
    }}

}
</script>
<style scoped>

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.screen{
    display: flex;
}

/*
.form{

}
*/

.form_tittle{
    color: #fff;
}





</style>