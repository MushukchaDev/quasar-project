<template>
    <div class="q-gutter-md" style="max-width: 300px">

        <q-input outlined v-model="text" dense label="C" />
        <q-input outlined v-model="text1" dense label="По" />
        <q-input outlined v-model="text2" dense label="C" />
        <q-input outlined v-model="text3" dense label="По" />
        <q-input outlined v-model="text4" dense label="Ограничить кол-во" />
        <q-input outlined v-model="text5" dense label="Имеет статус" />
        <q-input outlined v-model="text6" dense label="Статус не равен" />
        <q-select outlined v-model="modelMultiple" multiple :options="tags" dense use-chips stack-label options-dense
            label="Имеет теги">
        </q-select>
        <q-select outlined v-model="modelMultiple1" multiple :options="tags" dense options-dense stack-label use-chips
            label="Не имеет теги">
        </q-select>

        <q-select outlined v-model="model" :options="pole_dati" dense options-dense label="Поле даты">
        </q-select>
        <q-select outlined v-model="model1" :options="sortirovat" dense options-dense label="Сортировать по"></q-select>
        <q-select outlined v-model="modelMultiple2" multiple :options="tipi" dense stack-label options-dense use-chips
            label="Типы событий">
        </q-select>
        <q-checkbox dense v-model="obrat_sort" label="Обратная сортировка" color="dark" />
        <q-select outlined v-model="model2" :options="vibrat" dense options-dense label="Выбрать">
        </q-select>
    </div>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'RashFiltr',

    setup() {
        return {
            model: ref(null),
            model1: ref(null),
            model2: ref(null),
            drawer: ref(false),
            obrat_sort: ref(false),
            modelMultiple: ref(['Холодный звонок']),
            modelMultiple1: ref(['Холодный звонок']),
            modelMultiple2: ref(['Входящий']),
            pole_dati: [
                'Запланированная дата', 'meow', 'gav', 'кря'
            ],
            sortirovat: ['По дате', '123', '321'],
            tags: [
                'Холодный звонок', 'Клиент', 'Отказ', 'В разработке'
            ],
            tipi: ['Входящий', 'Исходящий', 'Пропущенный', 'Перезвонить'],
            vibrat: ['Все', 'Ничего'],
        }
    }
})
</script>
