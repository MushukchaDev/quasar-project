<template>
    <q-card class="crm-panel q-my-lg" style="">
        <q-card-section horizontal>

            <q-item class="crm-infopanel">
                <q-item-section>
                    <div class="text-subtitle1">Заметка в 16:26(понедельник)</div>
                    <q-item-label caption>
                        16 мая 2022г.
                    </q-item-label>
                    <div class="text-subtitle2 q-pt-md">1к на 1 этаже за 2900</div>

                </q-item-section>

                <q-item-actions class="q-pl-xl q-pr-none" align="right" side top>
                    <q-icon class="q-px-sm" size="20px" name="content_copy" />
                    <q-icon class="q-px-sm" size="20px" name="send" />
                    <q-icon class="q-px-sm" size="20px" name="grade" />
                    <q-icon class="q-px-sm" size="20px" name="close" />
                </q-item-actions>
            </q-item>
        </q-card-section>
    </q-card>
    <q-card class="q-my-lg">
        <q-card-section horizontal>
            <q-card-section class="bg-primary" style="width: 0.1px">
            </q-card-section>
            <q-item>
                <q-item-section>
                    <div class="text-h6">Созвон в 8:00 (вторник)</div>
                    <q-item-label caption>
                        17 мая 2022г.
                    </q-item-label>
                    <div class="text-subtitle3 q-pt-md"> </div>

                </q-item-section>

                <q-item-actions class="q-pl-xl q-pr-none" align="right" side top>
                    <q-icon class="q-px-sm" size="20px" name="content_copy" />
                    <q-icon class="q-px-sm" size="20px" name="send" />
                    <q-icon class="q-px-sm" size="20px" name="grade" />
                    <q-icon class="q-px-sm" size="20px" name="close" />
                </q-item-actions>
            </q-item>
        </q-card-section>
    </q-card>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'InfoPanel',

    setup() {
        return {
            obrat_sort: ref(false),
        }
    }
})
</script>
