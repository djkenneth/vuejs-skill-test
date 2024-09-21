<template lang="">
    <div class="relative-position circle-wrapper">
        <div class="circle-icon edeliver-icon">
          <img
            alt="circle edeliver"
            src="~assets/circle/edeliver.svg"
          >
        </div>
        <div class="circle-icon efood-icon">
          <img
            alt="circle efood"
            src="~assets/circle/efood.svg"
          >
        </div>
        <div class="circle-icon eservices-icon">
          <img
            alt="circle eservices"
            src="~assets/circle/eservices.svg"
          >
        </div>
        <div class="circle-icon emarket-icon">
          <img
            alt="circle emarket"
            src="~assets/circle/emarket.svg"
          >
        </div>
        <div class="absolute-center">
          <img
            alt="circle 911"
            src="~assets/circle/911.svg"
          >
        </div>
        <div class="circle-icon epayment-icon">
          <img
            alt="circle epayment"
            src="~assets/circle/epayment.svg"
          >
        </div>
        <div class="circle-icon eassist-icon">
          <img
            alt="circle eassist"
            src="~assets/circle/eassist.svg"
          >
        </div>
        <div class="circle-icon more-icon">
          <img
            alt="circle more"
            src="~assets/circle/more.svg"
          >
        </div>
        <div class="circle-icon egov-icon">
          <img
            alt="circle egov"
            src="~assets/circle/egov.svg"
          >
        </div>
      </div>
</template>
<script setup>
defineOptions({
    name: 'ManualCircle'
});
</script>
<style lang="scss">
  .circle-wrapper {
    margin-top: 4rem;
    // background-color: red;
    height: 22rem;
    position: relative;
    
    .circle-icon {
      position: absolute;
    }
    
    .edeliver-icon {
      left: 104px;
    }

    .efood-icon {
      left: 227px;
    }

    .eservices-icon {
      top: 53px;
      right: 53px;
    }

    .epayment-icon {
      bottom: 27px;
      right: -4px;
    }

    .more-icon {
      bottom: -1px;
      right: 106px;
    }

    .emarket-icon {
      top: 53px;
      left: 50px;
    }

    .eassist-icon {
      bottom: 27px;
      left: -2px;
    }

    .egov-icon {
      bottom: -2px;
      left: 103px;
    }

    @media screen and (max-width: 425px) {

      position: relative;

      // &::before {
      //   position: absolute;
      //   top: 0;
      //   left: 50%;
      //   bottom: 0;
      //   content: "";
      //   width: 1px;
      //   height: 100%;
      //   background-color: red;
      //   z-index: 1;
      // }

      // &::after {
      //   position: absolute;
      //   top: 50%;
      //   left: 0;
      //   content: "";
      //   width: 100%;
      //   height: 1px;
      //   background-color: red;
      //   z-index: 1;
      // }

      .edeliver-icon {
        top: 0px;
        left: 70px;
      }

      .efood-icon {
        top: 0px;
        left: 198px;
      }

      .eservices-icon {
        top: 54px;
        right: 16px;
      }

      .epayment-icon {
        bottom: 47px;
        right: 16px;
      }

      .more-icon {
        bottom: -4px;
        right: 70px;
      }

      .emarket-icon {
        top: 53px;
        left: 16px;
      }

      .eassist-icon {
        bottom: 48px;
        left: 16px;
      }

      .egov-icon {
        bottom: -4px;
        left: 70px;
      }
    }

    @media only screen and (max-width: 375px) {
      .edeliver-icon {
        top: 2px;
        left: 51px;
      }

      .efood-icon {
        top: 2px;
        left: 171px;
      }

      .eservices-icon {
        top: 54px;
        right: 0px;
      }

      .epayment-icon {
        bottom: 53px;
        right: 0px;
      }

      .more-icon {
        bottom: 2px;
        right: 49px;
      }

      .emarket-icon {
        top: 53px;
        left: 0px;
      }

      .eassist-icon {
        bottom: 53px;
        left: 0px;
      }

      .egov-icon {
        bottom: 2px;
        left: 50px;
      }
    }

    @media only screen and (max-width: 320px) {
      height: 16rem;

      img {
        width: 80%;
      }

      .edeliver-icon {
        top: -8px;
        left: 39px;
      }

      .efood-icon {
        top: -7px;
        left: 136px;
      }

      .eservices-icon {
        top: 33px;
        right: -6px;
      }

      .epayment-icon {
        bottom: 27px;
        right: -4px;
      }

      .more-icon {
        bottom: -13px;
        right: 35px;
      }

      .emarket-icon {
        top: 32px;
        left: -4px;
      }

      .eassist-icon {
        bottom: 27px;
        left: -2px;
      }

      .egov-icon {
        bottom: -14px;
        left: 39px;
      }
    }
  }
</style>