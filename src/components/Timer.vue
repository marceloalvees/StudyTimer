<template>
    <div class="is-flex is-align-items-center is-justify-content-space-between">
                    <StopWatch :timeInSeconds="timeInSeconds"/>
                    <button class="button" v-on:click="play" :disabled="StopWatchRunning">
                        <span class="icon">
                            <i class="fas fa-play"></i>
                        </span>
                        <span>Play</span>
                    </button>
                    <button class="button" @click="stop" :disabled="!StopWatchRunning">
                        <span class="icon">
                            <i class="fas fa-stop"></i>
                        </span>
                        <span>stop</span>
                    </button>
                </div>
</template>
<script lang="ts">
    import { defineComponent } from 'vue';
    import StopWatch from "./Stopwatch.vue"

    export default defineComponent({
        name:'TiMer',
        components:{
            StopWatch
        },
        data () {
            return{
                timeInSeconds: 0,
                cronometro: 0,
                StopWatchRunning: false

            }
        },
        methods: {
            play () {
                this.StopWatchRunning = true
                this.cronometro =  setInterval(() =>{
                    this.timeInSeconds += 1
                },1000)
            },
            stop () {
                this.StopWatchRunning = false
                clearInterval(this.cronometro)
            }
        }
    })
</script>