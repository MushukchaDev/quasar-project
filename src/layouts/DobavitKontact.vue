<template>
    <div class="q-gutter-md">

        <q-input color="accent" v-model="text" dense stack-label label="Имя" placeholder="Как зовут?" />
        <q-input color="accent" v-model="text1" dense stack-label label="Организация" placeholder="Где работает?" />
        <q-input color="accent" v-model="text2" dense stack-label label="Должность" placeholder="Кем работает?" />
        <q-checkbox color="accent" dense v-model="obrat_sort" stack-label label="Из адресной книги?" />
        <q-input color="accent" v-model="text4" dense stack-label label="Мобильный" placeholder="Номер телефона" />
        <q-btn color="accent" :ripple="false" dense unelevated label="Показать" no-caps />
        <q-btn class="text-dark" outline :ripple="false" dense unelevated label="Расширенный режим" no-caps />
        <q-btn color="accent" dense :ripple="false" label="Сохранить" no-caps />
        <q-btn class=" text-dark" dense outline :ripple="false" label="Сбросить" no-caps />
    </div>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'DobavitKontact',

    setup() {
        return {
            obrat_sort: ref(false),
        }
    }
})
</script>
