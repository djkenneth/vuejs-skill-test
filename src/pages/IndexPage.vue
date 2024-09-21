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

<template>
  <q-page clas="relative-position">
    <div class="main-wrapper">
      <div class="layer2-wrapper">
        <div class="layer-wrapper">
          <img alt="home" src="~assets/camera.svg" class="home-button-wrapper">
          <div class="content">
            <q-input rounded standout type="search" v-model="search" label="Search">
              <template v-slot:prepend>
                <q-icon name="menu" />
              </template>
              <template v-slot:append>
                <q-icon name="search" />
              </template>
            </q-input>
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
                <q-linear-progress size="5px" :value="progress" color="primary" track-color="cyan" />
              </div>
              <p class="profile-description">Complete your profile to access all Verified Citizen Privileges</p>
            </div>
          </div>
        </div>
      </div>
    </div>

  </q-page>
</template>


<style lang="scss" scoped >
.main-wrapper {
  position: relative;
  width: 100%;
  height: 100vh;

  .layer2-wrapper {
    background-image: url("layer2.svg");
    background-repeat: no-repeat;
    background-size: 450px;
    width: 100%;
    height: 100vh;
    background-position-x: center;
    position: relative;

    .layer-wrapper {
      position: absolute;
      top: 18px;
      left: 0;
      background-image: url('layer.svg');
      background-repeat: no-repeat;
      background-size: inherit;
      background-position-x: center;
      width: 100%;
      height: inherit
    }

    .home-button-wrapper {
      width: 35px;
      height: 35px;
      position: absolute;
      top: 28px;
      left: 50%;
      transform: translate(-50%, -50%);
    }

    .content {
      position: relative;
      padding-top: 4rem;
      max-width: 90%;
      margin: auto;

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
        padding-bottom: 5rem;

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
  }
}
</style>