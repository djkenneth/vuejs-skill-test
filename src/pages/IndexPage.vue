<template>
  <q-page clas="relative-position">
    
    <div class="wrapper">
        <img
          alt="home"
          src="~assets/camera.svg"
          class="home-button-wrapper"
        >
      <q-input rounded standout type="search" v-model="search" label="Search">
        <template v-slot:prepend>
          <q-icon name="menu" />
        </template>
        <template v-slot:append>
          <q-icon name="search" />
        </template>
      </q-input>
      <!-- <ManualCircle /> -->
      <Circle />
      <div class="intro">
        <h3 class="intro-title">911 Call Emergency</h3>
        <p class="intro-description">
          Call emergency on the City Hotline or report crime and emergency situations in Realtime response.
        </p>
      </div>

      <div class="profile">
        <p class="profile-title">Profile Completion</p>
        <div class="progress">
          <q-linear-progress
            size="5px"
            :value="progress"
            color="primary"
            track-color="cyan"
          />
        </div>
        <p class="profile-description">Complete your profile to access all Verified Citizen Privileges</p>
      </div>
    </div>
  </q-page>
</template>

<script setup>
// import ManualCircle from '../components/ManualCircle.vue'
import Circle from '../components/Circle.vue'
import { ref } from 'vue'

defineOptions({
  name: 'IndexPage'
});

const search = ref('')
const progress = ref(0.2)
</script>
<style lang="scss">
  .home-button-wrapper {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 45px;
      height: 45px;
      position: absolute;
      top: -2px;
      left: 50%;
      transform: translate(-50%, -50%);
    }

  .wrapper {
  position: relative;
  padding: 3.5rem 1rem 2rem 1rem;
  background-color: #F7FAFC;
  margin-top: 3rem;
  box-shadow: 0 -5px 15px 1px #087F9640;


    &::before {
      content: "";
      position: absolute;
      height: 80px;
      width: 80px;
      background-color: #F7FAFC;
      top: -2px;
      left: 50%;
      border-radius: 100%;
      transform: translate(-50%, -50%);
      box-shadow: 0 -5px 15px 1px #087F9640;
    }

    .intro {
      &-title {
        text-align: center;
        font-size: 2.2rem;
        color: #00687B;
        margin-bottom: 18px;
      }

      &-description {
        text-align: center;
        font-size: 16px;
      }
    }

    .profile {
      &-title {
        text-align: center;
        font-size: 1rem;
        font-weight: 500;
        color: #00687B;
      }
      .progress {
        display: flex;
        align-items: center;
        gap: 20px;
      }
      &-description {
        text-align: center;
        font-weight: 500;
        font-size: 0.8rem;
        padding-top: 10px;
        color: '#000';
      }
    }
  }


  
</style>

