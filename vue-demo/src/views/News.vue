<template>
  <div>
    <h2>这是新闻页面</h2>
    <h3>使用 params 传递参数</h3>
    <ul>
      <li v-for="item in newslist" :key="item.id">
        <router-link
          :to="{name: 'newsdetail', params: { id: item.id, title: item.title}}"
        >
        {{item.title}}
        </router-link>
      </li>
    </ul>
    <h3>使用 query 传递参数</h3>
    <ul>
      <li v-for="item in newslist" :key="item.id">
        <router-link
          :to="{name: 'newsdetail', query: { id: item.id, title: item.title}}"
        >
        {{item.title}}
        </router-link>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "news",
  data: () => {
    return {
      newslist: [
        { id: 1, title: "新闻1" },
        { id: 2, title: "新闻2" },
        { id: 3, title: "新闻3" },
        { id: 4, title: "新闻4" }
      ]
    };
  }
};
</script>
<style scoped>
</style>


