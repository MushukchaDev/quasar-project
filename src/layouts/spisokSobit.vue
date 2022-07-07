<template>
    <q-card class="my-card" flat square bordered>
        <div class="row">
            <div class=" col q-pt-sm q-pl-sm">
                <q-input square outlined v-model="text" dense />
            </div>
            <div class=" col-1">
                <p class="crm-center-word">
                    По
                </p>
            </div>
            <div class=" col q-pt-sm q-pr-sm">
                <q-input square outlined v-model="text" dense />
            </div>
        </div>
        <div class="row">
            <q-card-actions class="flex q-px-lg">
                <q-btn :ripple="false" unelevated color="indigo-9" label="Показать" no-caps />
                <q-btn outline :ripple="false" unelevated color="indigo-9" label="Расширенный режим" no-caps />
            </q-card-actions>
        </div>
    </q-card>
    <q-card class="q-mt-lg" flat square bordered>

        <q-list>
            <q-item class="crm-events-datelabel">
                <q-item-label>День</q-item-label>
            </q-item>
            <!--Первый пример-->
            <q-item horizontal>
                <q-item-section avatar>
                    <q-icon class="text-weight-bolder" color="Navy" name="arrow_upward" />
                </q-item-section>
                <q-item-section>
                    <q-item-label>Item with caption</q-item-label>
                    <q-item-label caption>Caption</q-item-label>
                </q-item-section>
                <q-item-section class="text-caption" side top>0:00</q-item-section>
            </q-item>

            <!--Второй пример-->
            <q-separator size="0.5px" />
            <q-item horizontal>
                <q-item-section avatar>
                    <q-icon class="text-weight-bolder" color="Navy" name="arrow_upward" />
                </q-item-section>
                <q-item-section>
                    <q-item-label>Item with caption</q-item-label>
                </q-item-section>
                <q-item-section class="text-caption" side top>12:42</q-item-section>
            </q-item>
            <!--Третий пример-->

            <q-separator size="0.5px" />
            <q-item horizontal>
                <q-item-section avatar>
                    <q-icon class="text-weight-bolder" color="Navy" name="arrow_downward" />
                </q-item-section>
                <q-item-section>
                    <q-item-label>Item with caption</q-item-label>
                </q-item-section>
                <q-item-section class="text-caption" side top>11:11</q-item-section>
            </q-item>
        </q-list>



    </q-card>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'SpisokSobit',

    setup() {
        return {
            model: ref(null),
            dense: ref(true),
            drawer: ref(false)
        }
    }
})
</script>
