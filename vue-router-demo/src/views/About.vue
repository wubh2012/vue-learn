<template>
  <div>
    <h2>关于页面</h2>
    <button @click="redirect">点击跳转到News页面</button>
  </div>
</template>

<script>
import router from '@/router'
export default {
  name: 'about',
  methods: {
    redirect: (event)=>{
      console.log('button click', this, event)
      
      console.log('router', router)
      // router.push({ name: 'news'})
      router.push({ name: 'newsdetail', query: { id: 100, title: '啦啦啦德玛西亚'}})
    }
  }
}
</script>
