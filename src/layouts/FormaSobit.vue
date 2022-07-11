<template>
    <div class=" q-pa-md q-gutter-sm">
        <q-btn label="Close Icon" color="primary" @click="icon = true" />

        <q-dialog v-model="icon">
            <q-card style="max-width:400px">
                <q-card-section class="q-pb-none">

                    <div class="row items-center ">
                        <div class="text-h6">Форма событий</div>
                        <q-space />
                        <q-btn icon="close" flat round dense v-close-popup />
                    </div>
                </q-card-section>
                <q-card-section>
                    <div class="row">
                        <div class="col-12">
                            <q-select :options-dense='true' dense color="accent" v-model="model" :options="deist"
                                label="Действие" />
                        </div>
                        <div class="col-6">
                            <q-input color="accent" dense v-model="date" mask="date" :rules="['date']">
                                <template v-slot:append>
                                    <q-icon name="event" class="cursor-pointer">
                                        <q-popup-proxy cover transition-show="scale" transition-hide="scale">
                                            <q-date color="warning" v-model="date">
                                                <div class="row items-center justify-end">
                                                    <q-btn v-close-popup label="ОК" color="accent" flat />
                                                </div>
                                            </q-date>
                                        </q-popup-proxy>
                                    </q-icon>
                                </template>
                            </q-input>
                        </div>
                        <div class="col-4 offset-2">
                            <q-input color="accent" dense v-model="time" mask="time" :rules="['time']">
                                <template v-slot:append>
                                    <q-icon name="access_time" class="cursor-pointer">
                                        <q-popup-proxy cover transition-show="scale" transition-hide="scale">
                                            <q-time color="warning" v-model="time">
                                                <div class="row items-center justify-end">
                                                    <q-btn v-close-popup label="ОК" color="accent" flat />
                                                </div>
                                            </q-time>
                                        </q-popup-proxy>
                                    </q-icon>
                                </template>
                            </q-input>

                        </div>
                        <div class="col-12">

                            <q-input color="accent" v-model="text" dense outlined type="textarea" />
                            <q-chip dense square color="accent" text-color="white">
                                Результат
                            </q-chip>
                            <q-chip dense square color="accent" text-color="white">
                                Договориться
                            </q-chip>
                        </div>
                        <div class="col-12">
                            Файлы
                        </div>
                        <div class="col-12">
                            <q-checkbox dense color="accent" v-model="right" label="Сделано" />
                        </div>
                    </div>
                </q-card-section>
                <q-card-actions>
                    <q-btn :ripple="false" icon="attach_file" label="Прикрепить" color="accent" />
                    <q-space />
                    <q-btn :ripple="false" class="bg-white text-dark" label="Отмена" />
                    <q-btn :ripple="false" label="Сохранить" color="accent" />
                </q-card-actions>
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
            date: ref('2022/01/01'),
            dense: ref(true),
            denseOpts: ref(true)
        }
    }
})
</script>
