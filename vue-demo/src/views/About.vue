<template>
  <div>
    <h2>关于页面</h2>
    <button @click="redirect">点击跳转到NewsDetail页面</button>
    <br>
    <br>
    <br>
    <br>
    <input type="txet" placeholder="请输入文字" v-model="msg" @keypress.enter="enter">
    <p>{{upper}}</p>

  </div>
</template>

<script>
import router from '@/router'
export default {
  name: 'about',
  data(){
    return {
      msg: 'about msg'
    }
  },
  methods: {
    redirect: (event) => {
      debugger
      console.log('单文件组件中的this', this) // 输出 undefined
      console.log(event)
      // console.log('router', router)
      // router.push({ name: 'news'})
      //router.push({ name: 'newsdetail', query: { id: 100, title: '啦啦啦德玛西亚'}})
    },
    enter () {
      alert(this.msg);
    }
  },
  computed: {
    upper () {
      return this.msg.toUpperCase();
    }
  }
}
</script>
