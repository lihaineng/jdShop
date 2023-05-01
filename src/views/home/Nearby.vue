<template>
    <div class="nearby">
        <h3 class="nearby__title">附近店铺</h3>
        <ShopInfo 
        v-for="item in nearbyList"
        :key="item._id"
        :item="item"
        />
    </div>
</template>

<script>
import { ref } from 'vue'
import { get } from '../../utils/request'
import ShopInfo from '../../components/ShopInfo'

const usetNearbyListEffect = () => {
    const nearbyList = ref([]) // 存储附近店铺列表的变量，用于展示页面中附近店铺列表的展示
    const getNearbyList = async () => { 
        const result = await get('/api/shop/hot-list')
        if (result?.errno === 0 && result?.data?.length) {
            nearbyList.value = result.data
        }
    }
    return {nearbyList, getNearbyList}
}

export default{
    name: 'Nearby',
    components: { ShopInfo },
    setup() {
        const {nearbyList, getNearbyList} = usetNearbyListEffect()
        getNearbyList();
        return {nearbyList}
  }
}
</script>

<style lang="scss" scoped>
@import '../../style/viriables.scss';
.nearby {
    &__title {
        margin: .16rem 0 .02rem 0;
        font-weight: normal;
        font-size: .18rem;
        color: $content-fontcolor;
    }
}
</style>
