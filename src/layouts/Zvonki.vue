<template>
    <div class="q-pa-md row justify-left">
        <q-card style="width: 100%; max-width: 350px">
            <q-chat-message class="q-pr-md q-py-sm" bg-color="indigo-1" sent stamp="29.06 11:30">
                <div class="text-subtitle1"> </div>
            </q-chat-message>
            <q-chat-message class="q-pl-md q-py-sm" bg-color="indigo-3" stamp="сегодня  12:10">
                <div class="text-subtitle1"> </div>
            </q-chat-message>
            <q-chat-message class="q-pl-md q-py-sm q-pr-xl" bg-color="indigo-3" stamp="сегодня 12:10">
                <div>
                    <q-btn :ripple="false" round color="indigo-7" icon="play_arrow" />
                    ----------------------------
                </div>
            </q-chat-message>
        </q-card>
    </div>
</template>
<style>
</style>
<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'ZvonkiPanel',

    setup() {
        return {
            obrat_sort: ref(false),
        }
    }
})
</script>
