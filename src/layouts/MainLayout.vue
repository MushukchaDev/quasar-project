<template>
  <q-layout view="hHh lpR fFf" style="fullheight" class="shadow-2 rounded-borders fullpage">
    <q-header elevated class="bg-white">
      <q-toolbar>
        <q-btn flat @click="drawer = !drawer" round dense icon="menu" class="text-dark"></q-btn>
        <q-toolbar-title class="text-dark">
          <q-input borderless v-model="text" label="Часть имени" />
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-footer elevated class="bg-grey-8">
      <div class="row justify-center">
        <div class="col-md-8">
          <q-btn size="md" padding="xs" icon="launch" />
          <q-btn size="md" padding="xs" icon="message" />
        </div>

        <div>
          <q-btn size="md" padding="xs" icon="note" />
          <q-btn size="md" padding="xs" icon="phone" />
          <q-btn size="md" padding="xs" icon="add" />
        </div>
      </div>
    </q-footer>

    <q-drawer v-model="drawer" show-if-above :width="200" :breakpoint="400">
      <q-scroll-area style="height: calc(100% - 200px); margin-top: 200px;">
        <q-list padding>

          <q-item clickable>
            <q-item-section active-class="q-item-no-link-highlighting">
              Журнал
            </q-item-section>
          </q-item>

          <q-item clickable>
            <q-item-section active-class="q-item-no-link-highlighting">
              Последний звонок
            </q-item-section>
          </q-item>

          <q-item clickable>
            <q-item-section active-class="q-item-no-link-highlighting">
              Контакты
            </q-item-section>
          </q-item>

          <q-expansion-item label="Поиски">
            <q-list class="q-pl-lg">
              <q-item clickable active-class="q-item-no-link-highlighting">
                <q-item-section>
                  <q-item-label>Добавить</q-item-label>
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
          <div class="text-weight-bold text-dark">МАРИЯ ВЛАДИМИРОВНА</div>
          <div>
            <q-select borderless dence options-dense v-model="model" :options="options2" />
          </div>
        </div>
      </q-img>
    </q-drawer>

    <q-page-container>
      <q-page padding horizontal>
        <ZvonkiPanel />
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
console.log(SpisokSobit)
export default defineComponent({
  name: 'MainLayout',
  components: { ZvonkiPanel },

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
