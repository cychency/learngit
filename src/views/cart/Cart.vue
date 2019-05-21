<template>
    <div>
        <van-nav-bar title="购物车" left-text="返回" @click-left="$router.go(-1)" left-arrow>
            <van-icon name="search" slot="right">
        </van-nav-bar>
        <h1>购物车</h1>
        <p v-for="(item,index) in goods" :key="index">{{item.name}}--{{item.num}}</p>
    </div>
</template>
<script>
// 导入mapstate方法
import {mapState} from 'vuex';
import {NavBar,Icon}from 'vant';
export default {
    computed:{
        ...mapState(["goods"])
    },
    comments:{
        [NavBar.name]:NavBar,
        [Icon.name]:Icon
    }
}
</script>
<style scoped>

</style>
