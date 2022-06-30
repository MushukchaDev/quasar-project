<template>
    <q-card class="my-card" flat square bordered>
        <q-card-section class="q-pt-lg q-px-lg" horizontal>
            <q-input square outlined v-model="text" :dense="dense" />
            <p class="q-mt-sm q-px-sm">
                По
            </p>
            <q-input square outlined v-model="text" :dense="dense" />
        </q-card-section>
        <q-card-actions class="flex q-px-lg">
            <q-btn :ripple="false" unelevated color="indigo-9" label="Показать" no-caps />
            <q-btn outline :ripple="false" unelevated color="indigo-9" label="Расширенный режим" no-caps />
        </q-card-actions>
    </q-card>
    <q-card class="my-card2 q-mt-lg" flat square bordered>
        <q-item-section style="background:#f0f0f0">
            <q-item-section>
                <q-item-label class="q-px-md q-py-xs" style="color:DimGray">День</q-item-label>
            </q-item-section>
        </q-item-section>
        <q-list>
            <!--Первый пример-->
            <q-item horizontal>
                <q-item-section avatar>
                    <q-icon color="Navy" name="arrow_upward" />
                </q-item-section>
                <q-item-section>
                    <div class="text-h8 q-mt-xs q-mb-none">Имя</div>
                    <div class="text-caption text-grey">Подпись снизу</div>
                </q-item-section>
                <q-item-section class="text-caption" side top>0:00</q-item-section>
            </q-item>

            <!--Второй пример-->
            <q-separator size="0.5px" />
            <q-item horizontal>
                <q-item-section avatar>
                    <q-icon color="Navy" name="arrow_upward" />
                </q-item-section>
                <q-item-section>
                    <div class="text-h8 q-mt-xs q-mb-none">+7228228228</div>
                </q-item-section>
                <q-item-section class="text-caption" side top>12:42</q-item-section>
            </q-item>
            <!--Третий пример-->

            <q-separator size="0.5px" />
            <q-item horizontal>
                <q-item-section avatar>
                    <q-icon color="Navy" name="arrow_downward" />
                </q-item-section>
                <q-item-section>
                    <div class="text-h8 q-mt-xs q-mb-none">+7228228228</div>
                </q-item-section>
                <q-item-section class="text-caption" side top>11:11</q-item-section>
            </q-item>
        </q-list>
    </q-card>
    <q-card class="my-card-2">

    </q-card>


</template>

<style lang="sass" scoped>
.my-card
  width: 400px
  min-height: 130px
  max-height: 140px
.my-card2
  width: 400px
.my-card3
  width: 400px

</style>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'SpisokSobit',

    setup() {
        return {
            model: ref(null),
            dense: ref(true),
            drawer: ref(false)
        }
    }
})
</script>
