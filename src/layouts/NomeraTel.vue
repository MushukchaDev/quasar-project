<template>
    <div class="q-gutter-md" style="max-width: 300px">

        <q-input outlined v-model="text" dense stack-label label="Имя" placeholder="Как зовут?" />
        <q-input outlined v-model="text1" dense stack-label label="Организация" placeholder="Где работает?" />
        <q-input outlined v-model="text2" dense stack-label label="Должность" placeholder="Кем работает?" />
        <q-checkbox dense v-model="obrat_sort" stack-label label="Из адресной книги?" color="indigo-5" />
        <q-input outlined v-model="text4" dense stack-label label="Мобильный" placeholder="Номер телефона" />
        <q-btn :ripple="false" color="indigo-5" label="Сохранить" no-caps />
        <q-btn :ripple="false" outline color="indigo-5" label="Сбросить" no-caps />
    </div>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'NomeraTel',

    setup() {
        return {
            obrat_sort: ref(false),
        }
    }
})
</script>
