<template>
  <div class="wrapper">
    <ul class="content">
      <button @click="btnClick">按钮</button>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
      <li>heihei</li>
    </ul>
  </div>
</template>

<script>
  import BScroll from 'better-scroll'
    export default {
        name: "Category",
        data() {
            return {
                scroll:null
            }
        },
        mounted() {
            this.scroll = new BScroll('.wrapper',{
                probeType: 3,
                pullUpLoad: true
            })

            this.scroll.on('scroll', (position) => {
                console.log(position);
            })

            this.scroll.on('pullingUp', () => {
                console.log('上拉加载更多');
            })
        },
        methods: {
          btnClick(){
              console.log('按钮点击');
          }
        }
    }
</script>

<style scoped>
  .wrapper {
    height: 100px;
    background-color: red;
  }

</style>
