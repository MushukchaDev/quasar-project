<template>
    <q-card class="q-gutter-sm" style="max-width: 400px">
        <q-item>
            <q-item>
                <h5 class="text-justify">Редактировать контакт</h5>
            </q-item>
            <q-item side top>
                <q-icon name="close" />
            </q-item>
        </q-item>
        <q-item>
            <div class="q-gutter-sm q-px-xs" style="max-width: 400px">

                <q-input outlined v-model="text" dense stack-label label="Имя" placeholder="Как зовут?" />
                <q-input outlined v-model="text1" dense stack-label label="Организация" placeholder="Где работает?" />
                <q-input outlined v-model="text2" dense stack-label label="Должность" placeholder="Кем работает?" />
                <q-checkbox dense v-model="obrat_sort" stack-label label="Из адресной книги?" color="indigo-5" />
                <q-checkbox dense v-model="obrat_sort2" stack-label label="Сохранить в новую версию" color="indigo-5" />


            </div>
        </q-item>
        <q-item class="q-pb-lg">
            <div class="q-gutter-sm q-px-xs" style="max-width: 400px">
                <q-btn :ripple="false" color="red" label="Удалить" no-caps />
                <q-btn class="q-ml-xl" :ripple="false" color="indigo-5" label="Сохранить" no-caps />
                <q-btn :ripple="false" outline color="indigo-5" label="Сбросить" no-caps />
            </div>
        </q-item>

    </q-card>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'DannieCont',

    setup() {
        return {
            obrat_sort: ref(false),
            obrat_sort2: ref(false),
        }
    }
})
</script>
