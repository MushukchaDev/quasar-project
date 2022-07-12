
<template>
  <q-layout view="hHh lpR fFf" style="fullheight fullwidth" class="fullpage">
    <q-header reveal elevated class="bg-secondary">
      <q-toolbar>
        <q-btn flat @click="drawer = !drawer" round dense icon="menu" class="text-dark"></q-btn>
        <q-toolbar-title class="text-dark">
          <q-input borderless v-model="text" placeholder="Часть имени" />
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-footer elevated class="crm-footer bg-secondary q-pa-sm">
      <div class="row justify-center">
        <div class="col-md-8">

          <q-btn :ripple="false" class="bg-positive text-info" size="md" padding="xs" icon="launch" />
          <q-btn :ripple="false" class="bg-positive text-info" size="md" padding="xs" icon="message">
            <q-menu>
              <q-list dense style="min-width: 100px;">
                <q-item clickable v-close-popup>
                  <q-item-section>Whats up</q-item-section>
                </q-item>
                <q-item clickable v-close-popup>
                  <q-item-section>SMS</q-item-section>
                </q-item>
                <q-item clickable v-close-popup>
                  <q-item-section>Viber</q-item-section>
                </q-item>
              </q-list>
            </q-menu>
          </q-btn>

        </div>

        <q-btn :ripple="false" class="bg-positive text-info" size="md" padding="xs" icon="note" />
        <q-btn :ripple="false" class="bg-primary text-white" size="md" padding="xs" icon="phone" />
        <q-btn :ripple="false" class="bg-positive text-info" size="md" padding="xs" icon="add" />

        <!--<div>
          <q-btn class="bg-accent" size="md" padding="xs" icon="note" />
          <q-btn class="bg-accent" size="md" padding="xs" icon="phone" />
          <q-btn class="bg-accent" size="md" padding="xs" icon="add" />
        </div>-->

      </div>
    </q-footer>

    <q-drawer v-model="drawer" show-if-above :width="200" :breakpoint="400">
      <q-scroll-area class="bg-dark-page" style="height: calc(100% - 200px); margin-top: 170px;">
        <q-list padding class="crm-menu text-grey-8">

          <q-item clickable active-class="q-item-no-link-highlighting">
            <q-item-section>
              ЖУРНАЛ
            </q-item-section>
          </q-item>

          <q-item clickable active-class="q-item-no-link-highlighting">
            <q-item-section>
              ПОСЛЕДНИЙ ЗВОНОК
            </q-item-section>
          </q-item>

          <q-item clickable active-class="q-item-no-link-highlighting">
            <q-item-section>
              КОНТАКТЫ
            </q-item-section>
          </q-item>

          <q-expansion-item label="ПОИСКИ">
            <q-list>
              <q-item clickable active-class="q-item-no-link-highlighting">
                <q-item-section>
                  ДОБАВИТЬ
                </q-item-section>
              </q-item>
            </q-list>
          </q-expansion-item>
        </q-list>
      </q-scroll-area>

      <q-img class="absolute-top" style="height: 200px">
        <div class="absolute-center bg-transparent">
          <q-avatar size="56px" class="q-mb-sm">
            <img src="https://i.ibb.co/bzcmPP0/image.jpg">
          </q-avatar>
          <div class="text-weight-bold text-grey-8">МАРИЯ ВЛАДИМИРОВНА</div>
          <div>
            <q-select borderless dense options-dense v-model="model" :options="options2" />
          </div>
        </div>
      </q-img>
    </q-drawer>

    <q-page-container>
      <q-page padding horizontal>
        <div class="row">
          <div class="col= 'col-12 col-xl-6'">
            <NewPage />
          </div>
        </div>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EventList from './SpisokSobit.vue'
import RashFiltr from './RashFiltr.vue'
import DobavitKontact from './DobavitKontact.vue'
import ContactPage from './ContactPage.vue'
import InfoPanel from './InfoPanel.vue'
import ZvonkiPanel from './Zvonki.vue'
import FormaSobit from './FormaSobit.vue'
import NomeraTel from './NomeraTel.vue'
import DannieCont from './DannieCont.vue'
import NewPage from './NewPage.vue'
console.log(EventList)
export default defineComponent({
  name: 'MainLayout',
  components: { NewPage },

  setup() {


    return {
      model: ref(null),
      options2: [
        'Бренд-коуч'
      ],
      drawer: ref(false),
    }
  }
})
</script>
