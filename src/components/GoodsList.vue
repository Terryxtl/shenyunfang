<template>
  <div class="row">
    <div class="col-3 position-fixed">
      <ul class="">
        <li v-for="(item, index) in itemList" :key="index">
          <a :href="'#' + item.name">{{ item.name }}</a>
        </li>
      </ul>
    </div>
    <div class="col">
      <div
        class="row row-cols-2"
        v-for="(item, index) in itemList"
        :key="index"
      >
        <div
          class="col"
          v-for="(img, imgIndex) in item.imgList"
          :key="imgIndex"
          :id="item.name"
        >
          <img class="img-thumbnail" :src="img.imgUrl" loading="lazy" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      itemList: [
        {
          name: '亚克力挂件',
          imgList: [
            { imgUrl: '/image/3.1.webp' },
            { imgUrl: '/image/3.2.webp' }
          ]
        },
        {
          name: '贴纸',
          imgList: [
            { imgUrl: '/image/3.3.webp' },
            { imgUrl: '/image/3.4.webp' }
          ]
        },
        {
          name: '纸胶带',
          imgList: [
            { imgUrl: '/image/3.5.webp' },
            { imgUrl: '/image/3.6.webp' }
          ]
        },
        {
          name: '抱枕',
          imgList: [
            { imgUrl: '/image/3.7.webp' },
            { imgUrl: '/image/3.8.webp' },
            { imgUrl: '/image/3.9.webp' },
            { imgUrl: '/image/3.10.webp' }
          ]
        }
      ]
    }
  }
}
</script>

<style scoped>
ul {
  list-style: none;
}
</style>
