
<template>
    <div class="q-pa-md q-gutter-sm">
        <q-btn label="Close Icon" color="primary" @click="icon = true" />

        <q-dialog v-model="icon">
            <q-card style="width: 350px ;">

                <div class="row items-center q-pl-xs q-pb-xs">
                    <q-space />
                    <q-btn icon="close" color="black" flat round dense v-close-popup />
                </div>

                <div class="row items-center q-pl-xl q-pb-none">
                    <p>Редактировать контакт</p>
                </div>
                <q-tabs v-model="tab" dense class="text-brown-6 q-pl-md" :breakpoint="0" active-color="brown-10"
                    indicator-color="brown-10" align="left">
                    <q-tab name="osn" :class="tab == 'osn' ? 'text-black' : ''" label="Основная" />
                    <q-tab name="tel" :class="tab == 'tel' ? 'text-black' : ''" label="Телефоны" />

                </q-tabs>
                <q-tab-panels v-model="tab" animated>
                    <q-tab-panel name="osn" class="q-pa-sm">
                        <div class="row items-center q-pl-xs q-pb-xs">
                            <div class="q-gutter-sm q-px-xs" style="max-width: 300px">

                                <q-input v-model="text" label="Имя" placeholder="Как зовут?" stack-label dense />
                                <q-input v-model="text" label="Организация" placeholder="Где работает?" stack-label
                                    dense />
                                <q-input v-model="text" label="Должность" placeholder="Кем работает?" stack-label
                                    dense />

                                <q-checkbox dense v-model="obrat_sort" stack-label label="Из адресной книги?"
                                    color="dark-page" />
                                <q-checkbox dense v-model="obrat_sort2" stack-label label="Сохранить в новую версию"
                                    color="dark-page" />


                            </div>
                        </div>



                    </q-tab-panel>

                    <q-tab-panel name="tel" class="q-pa-sm">
                        <div class="row q-pl-md q-pb-xs" style="width: 300px">
                            <q-list>
                                <q-item horizontal>
                                    <q-item-section avatar>
                                        <q-avatar>
                                            <q-icon color="Navy" name="star" />
                                        </q-avatar>

                                    </q-item-section>
                                    <q-item-section>
                                        <div class="text-h6 q-mt-xs q-mb-none">+79610706572</div>
                                    </q-item-section>
                                    <q-item-section class="text-caption" side top>
                                        <q-icon color="Navy" name="more_vert" />
                                    </q-item-section>
                                </q-item>
                                <q-separator />
                            </q-list>
                        </div>
                        <div class="row q-pl-md q-pb-xs items-center" style="width: 300px">
                            <div class="col">
                                <q-input mask="(###) ### - ####" hint="(###) ### - ####" bottom-slots v-model="text"
                                    label="Номер телефона" dense>

                                    <template v-slot:append>
                                        <q-btn round dense flat icon="add" />
                                    </template>
                                </q-input>
                            </div>
                        </div>
                    </q-tab-panel>


                </q-tab-panels>
                <div class="row items-center  q-pl-lg q-pb-xs q-mb-lg" style="max-width: 300px">
                    <div class="q-gutter-sm q-px-xs" style="max-width: 300px">
                        <q-btn :ripple="false" unelevated style="max-width: 80px" color="teal-4" label="Удалить"
                            no-caps />
                        <q-btn class="q-ml-ms" unelevated style="max-width: 80px" :ripple="false" color="teal-3"
                            label="Сохранить" no-caps />
                        <q-btn :ripple="false" unelevated style="max-width: 80px" outline color="teal-3" label="Закрыть"
                            no-caps />
                    </div>
                </div>
            </q-card>
        </q-dialog>
    </div>
</template>

<style>
</style>
<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'DannieCont',

    setup() {
        return {
            model123: ref(null),
            tab: ref('osn'),
            icon: ref(false),
            obrat_sort: ref(false),
            obrat_sort2: ref(false),
            options2: ['+79610706572', '+79610706572', '+79610706572', '+79610706572']
        }
    }
})
</script>
