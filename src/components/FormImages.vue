<script setup lang="ts">
import type { Chaussure } from "@/types-images";
import { ref } from 'vue';
import { couleursNoms } from "@/types-images";
import Images from "./Images.vue";
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from "@headlessui/vue";

const chaussure = ref<Chaussure>({});
</script>

<template>
  <div>
    <TabGroup>
      <TabList class="tabs flex gap-1">
        <Tab class="tab tab-lifted ui-selected:tab-active">Côté</Tab>
        <Tab class="tab tab-lifted ui-selected:tab-active">Dessus</Tab>
        <Tab class="tab tab-lifted ui-selected:tab-active">Derrière</Tab>
      </TabList>
      <TabPanels class="w-64 p-2">
        <TabPanel>
          <Images v-bind="chaussure" class="w-full" />
        </TabPanel>
        <TabPanel>
          <Images v-bind="chaussure" class="w-full" orientation="dessus" />
        </TabPanel>
        <TabPanel>
          <Images v-bind="chaussure" class="w-full" orientation="derriere" />
        </TabPanel>
      </TabPanels>
    </TabGroup>
    <TabGroup>
    <FormKit
      type="form"
      v-model="chaussure"
    >
      <FormKit
        name="bandes"
        label="Bandes"
        type="select"
        :options="couleursNoms"
      />
    

    <FormKit
            name="cuir"
            label="cuir"
            type="select"
            :options="couleursNoms"
        />

    <FormKit
      name="mousse"
      label="Mousse"
      type="select"
      :options="couleursNoms"
    />
    </FormKit>
    </TabGroup>


  </div>
</template>
