<template>
    <div class="row q-gutter-md">
        <q-card>
            <q-card-section>
                <h1>Hello "h1"</h1>
            </q-card-section>
            <q-card-section>
                <div class="text-subtitle1">Hello "sub1"</div>
            </q-card-section>
            <q-card-section>
                <div class="text-body1">Hello "body1"</div>
            </q-card-section>
            <q-card-section>
                <div class="text-caption">Hello "capt"</div>
            </q-card-section>
        </q-card>
        <q-card>
            <q-card-section>
                <h2>Hello "h2"</h2>
            </q-card-section>
            <q-card-section>
                <div class="text-subtitle2">Hello "sub2"</div>
            </q-card-section>
            <q-card-section>
                <div class="text-body2">Hello "body2"</div>
            </q-card-section>
            <q-card-section>
                <div class="text-overline">Hello "body2"</div>
            </q-card-section>
        </q-card>
    </div>
</template>


<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
    name: 'NewPage',

    setup() {
        return {
            obrat_sort: ref(false),
        }
    }
})
</script>
