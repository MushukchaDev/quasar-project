
<template>
  <q-layout view="hHh lpR fFf" style="fullheight fullwidth" class="fullpage bg-primary">
    <q-header elevated class="bg-secondary">
      <q-toolbar>
        <q-btn flat @click="drawer = !drawer" round dense icon="menu" class="text-black"></q-btn>
        <q-toolbar-title class="text-dark">
          <q-input borderless v-model="text" label="Часть имени" />
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-footer elevated class="bg-secondary">
      <div class="row justify-center">
        <div class="col-md-8">
          <q-btn class="bg-dark" size="md" padding="xs" icon="launch" />


          <q-btn class="bg-dark" size="md" padding="xs" icon="message">
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

        <div>
          <q-btn class="bg-dark" size="md" padding="xs" icon="note" />
          <q-btn class="bg-dark" size="md" padding="xs" icon="phone" />
          <q-btn class="bg-dark" size="md" padding="xs" icon="add" />
        </div>
      </div>
    </q-footer>

    <q-drawer v-model="drawer" show-if-above :width="200" :breakpoint="400">
      <q-scroll-area class="bg-dark-page" style="height: calc(100% - 200px); margin-top: 200px;">
        <q-list padding>

          <q-item clickable>
            <q-item-section active-class="q-item-no-link-highlighting">
              ЖУРНАЛ
            </q-item-section>
          </q-item>

          <q-item clickable>
            <q-item-section active-class="q-item-no-link-highlighting">
              ПОСЛЕДНИЙ ЗВОНОК
            </q-item-section>
          </q-item>

          <q-item clickable>
            <q-item-section active-class="q-item-no-link-highlighting">
              КОНТАКТЫ
            </q-item-section>
          </q-item>

          <q-expansion-item label="ПОИСКИ">
            <q-list class="q-pl-lg">
              <q-item clickable active-class="q-item-no-link-highlighting">
                <q-item-section>
                  <q-item-label>ДОБАВИТЬ</q-item-label>
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
          <div class="text-weight-bold text-black">МАРИЯ ВЛАДИМИРОВНА</div>
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
            <DobavitKontact />
          </div>
        </div>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import SpisokSobit from './spisokSobit.vue'
import RashFiltr from './RashFiltr.vue'
import DobavitKontact from './DobavitKontact.vue'
import ContactPage from './ContactPage.vue'
import InfoPanel from './InfoPanel.vue'
import ZvonkiPanel from './Zvonki.vue'
import FormaSobit from './FormaSobit.vue'
import NomeraTel from './NomeraTel.vue'
import DannieCont from './DannieCont.vue'
console.log(SpisokSobit)
export default defineComponent({
  name: 'MainLayout',
  components: { DobavitKontact },

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
