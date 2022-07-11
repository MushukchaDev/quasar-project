<template>

    <div class="text-h4 q-pa-lg">Анастасия
        <q-icon name="create" />
    </div>
    <q-tabs v-model="tab" dense class="text-grey" :breakpoint="0" active-color="dark" indicator-color="dark"
        align="left">
        <q-tab name="calls" :class="tab == 'calls' ? 'text-dark' : ''" label="Звонки" />
        <q-tab name="info" :class="tab == 'info' ? 'text-dark' : ''" label="Информация" />
        <q-tab name="tags" :class="tab == 'tags' ? 'text-dark' : ''" label="Теги" />

    </q-tabs>

    <q-tab-panels v-model="tab" animated>
        <q-tab-panel name="calls" class="q-pa-sm">

            <q-item>
                привет
            </q-item>


        </q-tab-panel>

        <q-tab-panel name="info" class="q-pa-sm">
            <q-item>
                привет
            </q-item>
        </q-tab-panel>

        <q-tab-panel name="tags" class="q-pa-sm">
            <q-item>
                привет
            </q-item>
        </q-tab-panel>
    </q-tab-panels>

</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'ContactPage',

    setup() {
        return {
            tab: ref('calls'),

        }
    }
})
</script>
