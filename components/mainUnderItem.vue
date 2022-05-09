<template>
  <div class="underItem">
    <div class="underItem__wrapper">
      <img :src="getImgUrl(pic)" alt="item" class="underItem__pic" />
      <div class="underItem__main">
        <div class="underItem__title">{{ title }}</div>
        <div class="underitem__wrapper-subTitle">
          <img
            src="../static/underMainItems/underItem.svg"
            style="width: 45px"
            alt="vector"
          />
          <div class="underItem__subTitle">{{ subTitle }}</div>
        </div>

        <div class="underItem__text">{{ text }}</div>
        <div class="underItem__button">
          <button
            class="text-white not-italic text-base font-Circe bg-[#3865A7] hover:bg-[#1d4175] px-8 py-3 rounded-full"
          >
            <div class="underItem_button-arrow">
              <div style="padding-right: 13px">Читать историю</div>

              <img src="../static/underMainItems/arrow.svg" alt="arrow" />
            </div>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    pic: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    subTitle: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
  },
  data() {
    return {}
  },
  methods: {
    getImgUrl(pet) {
      const images = require.context(
        '../static/underMainItems',
        false,
        /\.svg$/
      )
      return images('./' + pet + '.svg')
    },
  },
}
</script>
<style>
.underItem__wrapper {
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
@media (max-width: 800px) {
  .underItem__wrapper {
    width: 40%;
  }
}
.underItem__pic {
  height: 320px;
  width: 460px;
  padding-right: 8%;
}
.underItem__main {
  width: 556px;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-items: flex-start;
  justify-content: center;
}
@media (max-width: 600px) {
  .underItem__main {
    width: 100vh;
  }
}
.underItem__title {
  font-weight: 700;
  font-size: 24px;
  line-height: 95.9%;
  padding-bottom: 22px;
}
.underitem__wrapper-subTitle {
  display: flex;
  align-items: center;
  flex-direction: row;
  padding-bottom: 15px;
}
.underItem__subTitle {
  padding-left: 19px;
  width: 490px;
  font-weight: 700;
  font-size: 16px;
  line-height: 122.4%;
  color: #fe5f5f;
}
@media (max-width: 800px) {
  .underItem__subTitle {
    width: 400px;
  }
}
.underItem__text {
  font-weight: 400;
  font-size: 16px;
  line-height: 115.4%;
  color: #000000;
  padding-bottom: 17px;
}
.underItem_button-arrow {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
}
</style>
