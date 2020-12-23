<template>
  <div class="coin-detail">
      <div v-for="(item, index) in detailDataList" :key="index" class="detail-item">
          <div class="col1">
              <p class="col1Title">{{item.text}}</p>
              <p class="col1text">{{item.date}}</p>
          </div>
          <div class="col2">
              +{{item.coinNum}}金币
          </div>
      </div>
  </div>
</template>
<script>
export default {
    data() {
        return {
          detailDataList: [
            {
              text: '关注话题',
              date: '2020/7/26',
              coinNum: 100
            },
            {
              text: '关注话题',
              date: '2020/7/26',
              coinNum: 100
            },
            {
              text: '关注话题',
              date: '2020/7/26',
              coinNum: 100
            },
            {
              text: '关注话题',
              date: '2020/7/26',
              coinNum: 100
            }
          ]
        }
    },
};
</script>

<style scoped>
  .coin-detail {

  }
  .detail-item {
      display: flex;
      padding: 1.6rem;
      justify-content: space-between;
  }
  .col1Title {
    font-family: PingFang SC;
    font-style: normal;
    font-weight: normal;
    font-size: 1.4rem;
    color: #303133;
    letter-spacing: 1px;
  }
  .col1text {
    font-family: PingFang SC;
    font-style: normal;
    font-weight: 300;
    font-size: 1rem;
    color: #606266;
    margin-top: 2px;
  }
  .col2 {
    font-family: PingFang SC;
    font-style: normal;
    font-weight: normal;
    font-size: 1rem;
    display: flex;
    align-items: center;
  }
</style>