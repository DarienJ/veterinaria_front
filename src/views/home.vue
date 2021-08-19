<template>
    <div class="formulario">
        <hr>
        <div class="completo">
            <h1 id="titulo_2"><strong>Administracion de pacientes</strong></h1>

            <div class="superior">
                <h2 id="titulo"><strong>Registro</strong></h2>
                    <input class="caja" type="text" v-model="nombre_mascota" placeholder="Nombre de mascota">                    <input class="caja" type="text" v-model="nombre_propietario" placeholder="Nombre propietario">
                    <input class="caja" type="text" v-model="telefono" placeholder="Telefono">
                    <input class="caja" v-model="fecha" type="date">
                    <input class="caja" v-model="tiempo" type="time">
                    <textarea class="caja" rows="5" v-model="dolencias" placeholder="Escribe las dolencias del animal"></textarea>
                    <input class="boton" @click='Enviar()' type="button" value="Enviar">
            </div>
            
            <div class="Inferior">
               <h1 id="titulo_3">Administracion de citas</h1>


            </div>

            <div class="fondo_2">
                <p></p>
            </div>

        </div>

        <div class="fondo">
            <p></p>

        </div>
    </div>    
</template>

<script>
import axios from 'axios'
export default {
    data(){
        return{
            nombre_mascota: '',
            nombre_propietario: '',
            telefono: '',
            tiempo: '',
            fecha: '',
            dolencias: ''
        }
    },

    methods: {

        Enviar(){
            axios.post(
                {
                    Nombre_Mascota: this.nombre_mascota,
                    Propietario: this.nombre_propietario,
                    Telefono: this.telefono,
                    Hora: this.tiempo,
                    Fecha: this.fecha,
                    Sintomas: this.dolencias
                }
            )
            alert('Funcionando')
        }
    }
}
</script>

<style scoped>

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

#titulo{
    color: #fff;
}

#titulo_2{
    color: #fff;
    margin-top: 80px;
}

#titulo_3{
    color: #fff;
    padding-top: 50px;
    padding-left: 40px;
}

.formulario{
    background: linear-gradient(to bottom, rgb(132, 39, 238), rgb(125, 192, 255));
}

.completo{
    background-color: #22004981;
    margin: auto;
    padding: auto;
    margin-left: 20px;
    margin-right: 20px;
    border-radius: 5px;
}

.superior{
    width: 300px;
    margin-top: 50px;
    margin-left: 480px;
    margin-right: auto;
    border-radius: 10px;
}

.caja{
    background:#ffffff;
    border: rgba(255, 255, 255, 0) 1px solid;
    border-bottom: #ccc 2px solid;
    padding: 8px;
    width:300px;
    color:#5d5d5d;
    margin-top:10px;
    font-size:1em;
    border-radius:4px;
}

.caja_2{
    background:#ffffff;
    border: rgba(255, 255, 255, 0) 1px solid;
    border-bottom: #ccc 2px solid;
    padding: 8px;
    width:210px;
    color:#5d5d5d;
    margin-top:10px;
    font-size:1em;
    border-radius:4px;   
}

.boton{
    margin-left:0px;
    margin-top: 10px;
    width: 300px;
    top: 100%;
    border-radius: 25px;
    padding-top:5px;
    padding-bottom:5px;
    background:#2ecc71;
    color:white;
    border-radius:4px;
    border-style: none;
}

.fondo{
    padding-top: 510px;
}

.fondo_2{
    padding-top: 50px;
}

.inferior{
    width: 300px;
    margin-top: 50px;
    margin-left: 480px;
    margin-right: auto;
    border-radius: 10px;
    padding-top: 50px;
}

</style>