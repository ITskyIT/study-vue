<template>
  <div class="hello">
    <h1>基础学习</h1>
    <span >文本插值：{{message}}</span>
    <button @click= "change()">点击改变插值</button>
    <p>html:</p>
    <span v-html="testHtml"></span>
  </div>
</template> 
<script>
export default {
  created () {
    console.log('a is' + this.a)
  },
  data () {
    return {
      a: 1,
      message: '这是插入的值',
      testHtml: '<span style="color: red">输出html</span>'
    }
  },
  methods: {
    change () {
      this.message = this.message + '1'
    }
  }
}
</script>