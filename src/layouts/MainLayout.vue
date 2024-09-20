<template>
  <q-layout view="lHh Lpr lFf" >
    <q-header class="bg-white">
      <q-toolbar class="flex justify-between">
        <img
          alt="CPA logo"
          src="~assets/logo.svg"
          style="width: 80px; height: 70px"
        >
        <div class="flex items-center icons">
          <img
              alt="Notification Icon"
              src="~assets/notification-icon.svg"
              class=""
              style="width: 20px"
            >
            <img
              alt="Dropdown Icon"
              src="~assets/dropdown-icon.svg"
              style="width: 15px"
            >
        </div>

      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
    <q-footer class="footer fixed-bottom bg-white q-px-sm q-py-sm">
        <div class="flex justify-between">
            <MenuIcon alt="menu profile" icon="profile" title="Profile" />
            <MenuIcon alt="menu messages" icon="messages" title="Messages" />
            <MenuIcon alt="menu home" icon="home" title="" />
            <MenuIcon alt="menu messenger" icon="messenger" title="Messenger" />
            <MenuIcon alt="menu activity" icon="activity" title="Activity" />
        </div>
    </q-footer>
  </q-layout>
</template>

<script setup>
import MenuIcon from '../components/MenuIcon.vue'
import { ref } from 'vue'

defineOptions({
  name: 'MainLayout'
})

// const leftDrawerOpen = ref(false)

// function toggleLeftDrawer () {
//   leftDrawerOpen.value = !leftDrawerOpen.value
// }
</script>

<style lang="scss">
.icons {
  gap: 15px;
}

.menu-col {
  gap: 20px;
}

.footer {
  box-shadow: 0 7px 9px -7px #087F9640 inset;
}
</style>
