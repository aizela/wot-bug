<template>
  <view class="patient-report-index">
    <wd-navbar title="健康知识" safeAreaInsetTop></wd-navbar>
    <wd-tabs v-model="tab" swipeable>
      <block v-for="item in tabs" :key="item.channelNo">
        <wd-tab :title="item.channelName" :name="item.channelNo"></wd-tab>
      </block>
    </wd-tabs>
  </view>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
const tab = ref('CCOO1')
const tabs = ref([
  {
    channelName: '推荐',
    channelNo: 'CC001'
  },
  {
    channelName: '默认频道',
    channelNo: 'pcc202408151038000001'
  },
  {
    channelName: '糖友锦囊嗷嗷',
    channelNo: 'pcc202408071731000001'
  },
  {
    channelName: '健康指导',
    channelNo: 'pcc202407291519000002'
  },
  {
    channelName: '科普专栏',
    channelNo: 'pcc20240721454000001'
  }
])
</script>
<style lang="scss" scoped></style>
