<template>
    <div class="q-pa-md q-gutter-sm">
        <q-btn label="Close Icon" color="primary" @click="icon = true" />

        <q-dialog v-model="icon">
            <q-card style="min-width: 300px ;">
                <div class="row items-center q-pl-lg q-pb-xs">
                    <q-space />
                    <q-btn icon="close" flat round dense v-close-popup />
                </div>

                <div class="row items-center q-pl-lg q-pb-xs">
                    <q-select style="min-width: 184px ;" outlined v-model="model" :options="deist" dense options-dense
                        label="Действие" />
                </div>
                <div horizontal class="row items-center q-pl-lg q-pb-xs ">
                    <q-input style="max-width: 100px;" outlined dense v-model="date" mask="date" :rules="['date']">
                        <template v-slot:append>
                            <q-icon name="event" class="cursor-pointer">
                                <q-popup-proxy cover transition-show="scale" transition-hide="scale">
                                    <q-date color="indigo-3" v-model="date">
                                        <div class="row items-center justify-end">
                                            <q-btn v-close-popup label="Закрыть" color="indigo-3" flat />
                                        </div>
                                    </q-date>
                                </q-popup-proxy>
                            </q-icon>
                        </template>
                    </q-input>
                    <q-input style="max-width: 100px;" outlined dense v-model="time" mask="time" :rules="['time']">
                        <template v-slot:append>
                            <q-icon name="access_time" class="cursor-pointer">
                                <q-popup-proxy cover transition-show="scale" transition-hide="scale">
                                    <q-time color="indigo-3" v-model="time">
                                        <div class="row items-center justify-end">
                                            <q-btn v-close-popup label="Закрыть" color="indigo-3" flat />
                                        </div>
                                    </q-time>
                                </q-popup-proxy>
                            </q-icon>
                        </template>
                    </q-input>

                </div>
                <div class="row items-center q-pl-lg q-pb-xs">
                    <q-input outlined dense v-model="text" autogrow />
                </div>
                <div class="row items-center q-pl-lg q-pb-xs">
                    <q-chip dense square color="indigo-5" text-color="white">
                        Результат
                    </q-chip>
                    <q-chip dense square color="indigo-5" text-color="white">
                        Договориться
                    </q-chip>
                </div>
                <div class="row items-center q-pl-lg q-pb-xs">
                    <q-file v-model="files" dense label="Файлы" outlined use-chips multiple style="max-width: 300px" />
                </div>
                <div class="row items-center q-pl-lg q-pb-xs">
                    <q-checkbox dense color="indigo-5" v-model="right" label="Сделано" />
                </div>
                <div class="row items-center q-pl-lg q-pb-xs">
                    <q-card-actions>
                        <q-btn dense :ripple="false" color="indigo-3" label="Отмена" no-caps />
                        <q-btn dense :ripple="false" color="indigo-5" label="Сохранить" no-caps />
                    </q-card-actions>
                </div>


            </q-card>
        </q-dialog>
    </div>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'FormaSobit',

    setup() {
        return {
            text: ref(''),
            icon: ref(false),
            right: ref(false),
            files: ref(null),
            model: ref(null),
            model1: ref(null),
            obrat_sort: ref(false),
            deist:
                ['Встреча', 'Звонок', 'хз'],
            time: ref('00:00'),
            date: ref('2022/01/01')
        }
    }
})
</script>
