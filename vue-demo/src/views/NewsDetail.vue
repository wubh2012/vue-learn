<template>
  <div>
    <h1>$route.params 信息</h1>
    <div>
      新闻ID: {{$route.params.id}}
      <br />
      新闻标题: {{$route.params.title}}
    </div>
    <hr />
    <h1>$route.query 信息</h1>
    <div>
      新闻ID: {{$route.query.id}}
      <br />
       新闻标题: {{$route.query.title}}
    </div>
  </div>
</template>
<script>
export default {
  name: "newsdetail"
};
</script>

