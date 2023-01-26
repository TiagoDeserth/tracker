<template>
    <Box>
        <div class="columns">
            <div class="column is-7">{{tarefa.descricao || 'Tarefa sem descrição'}}</div>
            <div class="column">
                <CronoMetro :tempoEmSegundos="tarefa.duracaoEmSegundos"/>
            </div>
        </div>
    </Box>
</template>

<script lang="ts">
import {defineComponent, PropType} from 'vue';
import CronoMetro from './Cronometro.vue'
import ITarefa from '../Interfaces/ITarefa'
import Box from './Box.vue'

export default defineComponent({
    name: 'TareFa',
    components: {
        CronoMetro,
        Box
    },
    props: {
        tarefa: {
            type: Object as PropType<ITarefa>,
            required: true
        }
    }
})
</script>
