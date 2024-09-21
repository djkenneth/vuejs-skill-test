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

<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white">
      <q-toolbar class="flex justify-between">
        <img alt="CPA logo" src="~assets/logo.svg" style="width: 80px; height: 70px">
        <div class="flex items-center icons">
          <img alt="Notification Icon" src="~assets/notification-icon.svg" class="" style="width: 20px">
          <img alt="Dropdown Icon" src="~assets/dropdown-icon.svg" style="width: 15px">
        </div>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
    <q-footer class="footer fixed-bottom bg-white q-px-sm q-pb-sm">
      <div class="flex justify-between menu-wrapper">
        <div class="menu-layer" style="display: flex; justify-content: space-between;"></div>
        <div class="menus">
          <MenuIcon alt="menu profile" icon="profile.svg" title="Profile" />
          <MenuIcon alt="menu messages" icon="messages.svg" title="Messages" />
        </div>
        <div class="menu-home-wrapper">
          <MenuIcon alt="menu home" icon="home.svg" title="" />
        </div>
        <div class="menus">
          <MenuIcon alt="menu messenger" icon="messenger.svg" title="Messenger" />
          <MenuIcon alt="menu activity" icon="activity.svg" title="Activity" />
        </div>


      </div>
    </q-footer>
  </q-layout>
</template>

<style lang="scss">
.icons {
  gap: 15px;
}

.menu-col {
  gap: 20px;
}

.footer {

  // box-shadow: 0 7px 9px -7px #087F9640 inset;
  .menu-wrapper {
    position: relative;
    overflow: hidden;
    padding-block: 3px;

    .menus {
      display: flex;
      align-items: center;
      gap: 25px
    }

    .menu-home-wrapper {
      position: absolute;
      left: 50%;
      transform: translate(-50%, -50%);
      top: 25px;
    }

    .menu-layer {
      position: absolute;
      background-image: url("./layer2.svg");
      background-repeat: no-repeat;
      background-size: 603px;
      width: 100%;
      height: 100px;
      background-position-y: bottom;
      background-position-x: center;
      bottom: -22px;
    }
  }
}

@media only screen and (max-width: 320px) {
  .footer {
    .menu-wrapper {
      .menus {
        display: flex;
        align-items: center;
        gap: 5px
      }
    }
  }
}
</style>
