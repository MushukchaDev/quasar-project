<template>
    <div class="q-pa-md q-gutter-sm">
        <q-btn label="Close Icon" color="primary" @click="icon = true" />

        <q-dialog v-model="icon">
            <q-card style="min-width: 300px ;">
                <q-card-section class="row items-center q-pb-none">
                    <q-space />
                    <q-btn icon="close" flat round dense v-close-popup />
                </q-card-section>

                <q-card-section>
                    <q-select style="max-width: 200px ;" outlined v-model="model" :options="deist" dense options-dense
                        label="Действие" />
                </q-card-section>
                <q-card-section horizontal class="q-pl-md">
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

                </q-card-section>
                <q-card-section>
                    <q-input outlined dense v-model="text" autogrow />
                    <q-chip dense square color="indigo-5" text-color="white">
                        Результат
                    </q-chip>
                    <q-chip dense square color="indigo-5" text-color="white">
                        Договориться
                    </q-chip>

                    <q-file v-model="files" dense label="Файлы" outlined use-chips multiple style="max-width: 300px" />

                    <q-checkbox dense color="indigo-5" v-model="right" label="Сделано" />
                    <q-card-actions>
                        <q-btn dense :ripple="false" color="indigo-3" label="Отмена" no-caps />
                        <q-btn dense :ripple="false" color="indigo-5" label="Сохранить" no-caps />
                    </q-card-actions>
                </q-card-section>

            </q-card>
        </q-dialog>
    </div>
    <!--<div class="q-gutter-md">
        <q-btn label="Close Icon" color="primary" @click="icon = true" />
        <q-dialog v-model="icon">
            <q-card>
                <q-card-section class=" row items-left q-pb-none" style="max-width: 300px">

                    <q-btn icon="close" flat round dense v-close-popup />
                </q-card-section>
                <q-card-section class="q-gutter-md " horizontal style="max-width: 300px">
                    <q-select outlined v-model="model" :options="deist" dense options-dense label="Действие" />
                    <q-input outlined dense v-model="date" mask="date" :rules="['date']">
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
                    <q-input outlined dense v-model="time" mask="time" :rules="['time']">
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

                    <q-input outlined dense v-model="text" type="textarea" />
                    <q-btn dense :ripple="false" color="indigo-5" label="Результат" no-caps />
                    <q-btn dense :ripple="false" color="indigo-5" label="Договориться" no-caps />

                    <q-file v-model="files" dense label="Файлы" outlined use-chips multiple style="max-width: 300px" />

                    <q-checkbox dense color="indigo-5" v-model="right" label="Сделано" />

                    <q-btn dense :ripple="false" color="indigo-3" label="Отмена" no-caps />
                    <q-btn dense :ripple="false" color="indigo-5" label="Сохранить" no-caps />
                </q-card-section>
            </q-card>
        </q-dialog>
    </div>-->
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
