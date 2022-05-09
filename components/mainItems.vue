<template>
  <div class="item">
    <div class="item__wrapper">
      <img :src="getImgUrl(pic)" alt="item" class="item__pic" />
      <div class="body__number">{{ number }}</div>
      <div class="body__text">{{ text }}</div>
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
    text: {
      type: String,
      required: true,
    },
    number: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {}
  },
  methods: {
    getImgUrl(pet) {
      const images = require.context('../static/mainItems', false, /\.svg$/)
      return images('./' + pet + '.svg')
    },
  },
}
</script>
<style>
.item__wrapper {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  flex-direction: column;
}
.item__pic {
  height: 190px;
}
.body__number {
  padding-top: 8px;
  font-weight: 700;
  font-size: 50px;
  line-height: 122.4%;
  color: #3865a7;
}
.body__text {
  font-weight: 700;
  font-size: 20px;
  line-height: 122.4%;
  text-align: center;
}
</style>
