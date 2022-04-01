<template src="./index.html" lang="html"></template>

<script lang="ts">
import {Component, Vue, Watch} from "vue-property-decorator";
import moment from "moment";

@Component
export default class Index extends Vue {
  title: string = "Hello fxbird"

  onLoad() {
    console.log(moment(new Date()).format("yyyy-MM-DD HH:mm:ss"))
    uni.showLoading({
      title: "加载中...."
    })

    setTimeout(()=>{uni.hideLoading()}, 2000)
  }
}
</script>

<style src="./index.scss" lang="scss"></style>
