<template>
    <div class="col-lg-6 col-md-6 col-sm-12 col-xs-12">

        <div class="text-h5">Анастасия
            <q-icon name="create" />
        </div>
        <q-tabs v-model="tab" dense class="text-grey" :breakpoint="0" active-color="grey" indicator-color="grey"
            align="left">
            <q-tab name="calls" :class="tab == 'calls' ? 'text-black' : ''" label="Звонки" />
            <q-tab name="info" :class="tab == 'info' ? 'text-black' : ''" label="Информация" />
            <q-tab name="tags" :class="tab == 'tags' ? 'text-black' : ''" label="Теги" />

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

    </div>
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
