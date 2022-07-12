<template>
    <q-card class="my-card" flat square bordered>
        <div class="row">
            <div class=" col q-pt-sm q-pl-sm">
                <q-input color="accent" square v-model="text" dense />
            </div>
            <div class=" col-1">
                <p class="crm-center-word">
                    По
                </p>
            </div>
            <div class=" col q-pt-sm q-pr-sm">
                <q-input color="accent" square v-model="text" dense />
            </div>
        </div>
        <div class="row">
            <q-card-actions class="flex q-px-lg q-pt-sm">
                <q-btn color="accent" :ripple="false" dense unelevated label="Показать" no-caps />
                <q-btn class="text-dark" outline :ripple="false" dense unelevated label="Расширенный режим" no-caps />
            </q-card-actions>
        </div>
    </q-card>
    <q-card class="q-mt-lg" flat square bordered>

        <q-list>
            <q-item class="crm-events-datelabel">
                <q-item-label class="text-grey-7">День</q-item-label>
            </q-item>
            <!--Первый пример-->
            <q-item class="crm-list" horizontal>
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
            <q-item class="crm-list" horizontal>
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
            <q-item class="crm-list" horizontal>
                <q-item-section avatar>
                    <q-icon class="text-weight-bolder" color="Navy" name="arrow_downward" />
                </q-item-section>
                <q-item-section>
                    <q-item-label>Item with caption</q-item-label>
                </q-item-section>
                <q-item-section class="text-caption" side top>11:11</q-item-section>
            </q-item>
        </q-list>

        <q-btn label="Hover me" color="primary">
            <q-tooltip>
                Some text as content of Tooltip
            </q-tooltip>
        </q-btn>

    </q-card>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'EventList',

    setup() {
        return {
            model: ref(null),
            dense: ref(true),
            drawer: ref(false)
        }
    }
})
</script>
