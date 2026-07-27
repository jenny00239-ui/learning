<script setup lang="ts">
const articles = [
  {
    to: '/article/2',
    title: '日本全家「FAMIMA」限定商品台灣也買得到！Convenience Wear聯名中筒襪、經典太陽星星Logo實用小物等12款新品'
  },
  {
    to: 'https://www.wowlavie.com/article/260027252',
    title: '伊東豊雄台南建築新作！「李科永紀念圖書館」以曲面環狀結構和綠意屋頂，築起象徵圓滿的閱讀天地'
  },
  {
    to: 'https://www.wowlavie.com/article/ae2200217',
    title: 'SWATCH紀念腕錶「女王駕到」！慶祝英國女王登基七十週年的白金禧時刻'
  },
  {
    to: 'https://www.wowlavie.com/article/260027229',
    title: '聶永真 ✕ HOUTH何婉君 ✕ Local Remote劉書堯對談品牌設計：從釐清定義、前期調研到提案策略，設計如何幫品牌走得更遠？'
  },
  {
    to: '/article/1',
    title: '2022瀨戶內國際藝術祭主視覺公開！男木島爺奶戴上墨鏡歡迎人們造訪'
  },
  {
    to: 'https://www.wowlavie.com/article/260027244',
    title: 'Dua Lipa 打造「禁書書店」Manifesto Library！從網路讀書會到實體圖書館，將閱讀變成一場公共行動'
  }
]
</script>

<template>
  <section class="hot-article">
    <h3>熱門文章</h3>

    <ol class="trending">
      <li
        v-for="(article, index) in articles"
        :key="article.to"
        class="trending-list"
      >
        <NuxtLink class="title" :to="article.to">
          <span class="rank">{{ index + 1 }}</span>
          <span>{{ article.title }}</span>
        </NuxtLink>
      </li>
    </ol>
  </section>
</template>

<style scoped>
.hot-article {
  display: flex;
  flex-direction: column;
  width: 300px;
}

h3 {
  display: flex;
  justify-content: center;
  font-size: 25px;
}

.trending {
  margin: 0;
  padding: 0;
}

.trending-list {
  padding: 14px 0;
  color: #202024;
  list-style: none;
  border-bottom: 1px solid #dedede;
  cursor: pointer;
  transition: color 0.2s ease;
}

.trending-list:first-child {
  border-top: 1px solid #dedede;
}

.title {
  display: flex;
  align-items: flex-start;
  color: inherit;
  line-height: 1.5;
  text-decoration: none;
}

.rank {
  flex-shrink: 0;
  margin-right: 12px;
  color: #c5ce66;
  font-family: "IBM Plex Sans", sans-serif;
  font-size: 30px;
  font-weight: 700;
  line-height: 1;
}

.trending-list:hover {
  color: #a9b53f;
}

.title:visited {
  color: inherit;
}
</style>
