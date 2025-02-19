<script setup>
    defineProps({
        cotizacion:{
            type: Object,
            required: true
        }
    })
</script>
<template>
    <div class="contenedor-resultado">
        <h2>Cotizacion</h2>
        <div class="resultado">
        <img :src="'https://cryptocompare.com' + cotizacion.IMAGEURL" alt="" />
        <div>
            <p>
            El precio es de: <span>{{ cotizacion.PRICE }}</span>
            </p>
            <p>
            El precio mas alto del día: <span>{{ cotizacion.HIGHDAY }}</span>
            </p>
            <p>
            El precio mas bajo del día <span>{{ cotizacion.LOWDAY }}</span>
            </p>
            <p>
            Variación ultimas 24 horas:
            <span>{{ cotizacion.CHANGEPCT24HOUR }}%</span>
            </p>
            <p>
            Última Actualización: <span>{{ cotizacion.LASTUPDATE }}</span>
            </p>
        </div>
        </div>
    </div>
</template>
