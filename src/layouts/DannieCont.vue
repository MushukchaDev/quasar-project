
<template>
    <div class="q-pa-md q-gutter-sm">
        <q-btn label="Close Icon" color="primary" @click="icon = true" />

        <q-dialog v-model="icon">
            <q-card style="width: 350px ;">

                <div class="row items-center q-pl-xs q-pb-xs">
                    <q-space />
                    <q-btn icon="close" color="dark" flat round dense v-close-popup />
                </div>

                <div class="row items-center q-pl-xl q-pb-none">
                    <p>Редактировать контакт</p>
                </div>
                <q-tabs v-model="tab" dense class="text-grey q-pl-md" :breakpoint="0" active-color="dark"
                    indicator-color="dark" align="left">
                    <q-tab name="osn" :class="tab == 'osn' ? 'text-dark' : ''" label="Основная" />
                    <q-tab name="tel" :class="tab == 'tel' ? 'text-dark' : ''" label="Телефоны" />

                </q-tabs>
                <q-tab-panels v-model="tab" animated>
                    <q-tab-panel name="osn" class="q-pa-sm">
                        <div class="row items-center q-pl-xs q-pb-xs">
                            <div class="q-gutter-sm q-px-xs" style="max-width: 300px">

                                <q-input color="accent" v-model="text1" label="Имя" placeholder="Как зовут?" stack-label
                                    dense />
                                <q-input color="accent" v-model="text2" label="Организация" placeholder="Где работает?"
                                    stack-label dense />
                                <q-input color="accent" v-model="text3" label="Должность" placeholder="Кем работает?"
                                    stack-label dense />

                                <q-checkbox dense v-model="obrat_sort" stack-label label="Из адресной книги?"
                                    color="accent" />
                                <q-checkbox dense v-model="obrat_sort2" stack-label label="Сохранить в новую версию"
                                    color="accent" />


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
                                <q-input color="accent" mask="(###) ### - ####" hint="(###) ### - ####" bottom-slots
                                    v-model="text7" label="Номер телефона" dense>

                                    <template v-slot:append>
                                        <q-btn round dense flat icon="add" />
                                    </template>
                                </q-input>
                            </div>
                        </div>
                    </q-tab-panel>


                </q-tab-panels>
                <q-card-actions>
                    <q-btn :ripple="false" label="Удалить" color="negative" />
                    <q-space />
                    <q-btn :ripple="false" class="bg-white text-dark" label="Закрыть" />
                    <q-btn :ripple="false" label="Сохранить" color="accent" />

                    <!--<q-btn :ripple="false" unelevated style="max-width: 80px" color="teal-4" label="Удалить" no-caps />
                    <q-btn class="q-ml-ms" unelevated style="max-width: 80px" :ripple="false" color="teal-3"
                        label="Сохранить" no-caps />
                    <q-btn :ripple="false" unelevated style="max-width: 80px" outline color="teal-3" label="Закрыть"
                        no-caps />-->

                </q-card-actions>
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
