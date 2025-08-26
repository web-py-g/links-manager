<script setup>
import { ref } from 'vue'

import Tabs from 'primevue/tabs'
import Tab from 'primevue/tab'
import TabList from 'primevue/tablist'
import TabPanel from 'primevue/tabpanel'
import TabPanels from 'primevue/tabpanels'
import LoginForm from './LoginForm.vue'
import RegistrationForm from './RegistrationForm.vue'
import ResetPasswordForm from './ResetPasswordForm.vue'

const activeTab = ref('signin') // signin | signup | reset
</script>

<template>
  <Tabs v-model:value="activeTab">
    <TabList>
      <Tab value="signin">Вход</Tab>
      <Tab value="signup">Регистрация</Tab>
    </TabList>

    <TabPanels>
      <TabPanel value="signin">
        <LoginForm @resetPassword="activeTab = 'reset'" />
      </TabPanel>
      <TabPanel value="signup">
        <RegistrationForm />
      </TabPanel>
      <TabPanel value="reset">
        <ResetPasswordForm />
      </TabPanel>
    </TabPanels>
  </Tabs>
</template>