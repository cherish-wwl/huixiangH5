<template>
  <div class="task">
    <div class="signBlock">
      <p class="signText">
        已签到{{signNum}}天
        <span class="signTip">（连续签到翻倍金币哦）</span>
      </p>
      <div class="coinItems">
        <div v-for="(item, index) in coin" :key="index" class="coinItem">
          <img />
          <span class="coinText1">{{item.text1}}</span>
          <p class="signTip">{{item.text2}}</p>
        </div>
      </div>
      <div class="signBtn">立即签到</div>
    </div>
    <div class="noviceBlock">
        <p class="taskTitle">新手任务</p>
        <div v-for="(item, index) in noviceDataList" :key="index" class="taskItems">
            <div class="noviceCol1">
                <img style="height: 32px;width: 32px;background-color:#ccc" />
            </div>
            <div class="noviceCol2">
                <p class="col2Title">{{item.title}}</p>
                <p class="col2text"><span class="col2CoinNum">+{{item.coinNum}}</span>金币</p>
            </div>
            <div class="noviceCol3">
                {{item.btnText}}
                <!-- <span class="col3Btn"></span> -->
            </div>
        </div>
    </div>
    <div class="everydayBlock">
        <p class="taskTitle">新手任务</p>
        <div v-for="(item, index) in noviceDataList" :key="index" class="taskItems">
            <div class="noviceCol1">
                <img style="height: 32px;width: 32px;background-color:#ccc" />
            </div>
            <div class="noviceCol2">
                <p class="col2Title">{{item.title}}</p>
                <p class="col2text"><span class="col2CoinNum">+{{item.coinNum}}</span>金币</p>
            </div>
            <div class="noviceCol3">
                {{item.btnText}}
                <!-- <span class="col3Btn"></span> -->
            </div>
        </div>
    </div>
    <div class="supplementTip">更多任务正在开启中敬请期待哦～</div>
  </div>
</template>
<script>
export default {
    data() {
        return {
            coin: [
                {
                    text1: 266,
                    text2: '今日'
                },
                {
                    text1: 366,
                    text2: '2天'
                },
                {
                    text1: 566,
                    text2: '3天'
                },
                {
                    text1: 666,
                    text2: '4天'
                },
                {
                    text1: 766,
                    text2: '5天'
                },
                {
                    text1: 866,
                    text2: '6天'
                },
                {
                    text1: '翻倍',
                    text2: '7天'
                },
            ],
            signNum: 0,
            noviceDataList: [
                {
                    title: '关注你喜欢的话题(0/1)',
                    coinNum: 100,
                    btnText: '已完成'
                },
                {
                    title: '关注你喜欢的话题(0/1)',
                    coinNum: 150,
                    btnText: '去完成'
                },
                {
                    title: '关注你喜欢的话题(0/1)',
                    coinNum: 200,
                    btnText: '领取'
                }
            ],
            everydayDataList: [
                {
                    title: '关注你喜欢的话题(0/1)',
                    coinNum: 100,
                    btnText: '已完成'
                },
                {
                    title: '关注你喜欢的话题(0/1)',
                    coinNum: 150,
                    btnText: '去完成'
                },
                {
                    title: '关注你喜欢的话题(0/1)',
                    coinNum: 200,
                    btnText: '领取'
                }
            ]
        }
    },
};
</script>

<style scoped>
    .task {
        background: linear-gradient(115.29deg, #2B71FF 1.19%, #807DFF 50.67%);
        padding: 0 10px;
        padding-top: 13rem;
        padding-bottom: 5rem;
    }
    .signBlock {
        background: #FFFFFF;
        border-radius: 12px;
        padding: 1.5rem;
    }
    .signText {
        font-size: 1.6rem;
        margin-bottom: 1.8rem;
    }
    .signTip {
        font-size: 1.2rem;
        color: #a7abb3;
        vertical-align: text-bottom;
    }
    .coinItems {
        display: flex;
        justify-content: space-between;
        
    }
    .coinItem {
        position: relative;
    }
    .coinText1 {
        position: absolute;
        width: 3rem;
        color: #FBBF64;
    }
    .signBtn {
        background: linear-gradient(90deg, #FF9500 0%, #FFDE6E 100%);
        border-radius: 60px;
        font-family: PingFang SC;
        font-style: normal;
        font-weight: normal;
        font-size: 18px;
        line-height: 3.6rem;
        color: #FFFFFF;
        width: 15rem;
        height: 3.6rem;
        text-align: center;
        margin: auto;
        margin-top: 2.2rem;
    }

    .noviceBlock {
        background: #FFFFFF;
        border-radius: 12px;
        padding: 1.5rem;
        margin-top: 1.6rem;
    }
    .taskTitle {
        font-family: PingFang SC;
        font-style: normal;
        font-weight: 500;
        font-size: 2rem;
    }
    .taskItems {
        display: flex;
        padding: 1.6rem 0;
    }
    .noviceCol1 {
        width: 12%;
    }
    .noviceCol2 {
        width: 67%;
    }
    .col2Title {
        font-family: PingFang SC;
        font-style: normal;
        font-weight: normal;
        font-size: 1.4rem;
        margin-top: -2px;
    }
    .col2text {
        font-family: PingFang SC;
        font-style: normal;
        font-weight: normal;
        font-size: 1rem;
        margin-top: 1px;
    }
    .col2CoinNum {
        color: #2D6DFF;
        margin-right: 2px;
    }
    .noviceCol3 {
        background: #C4C4C4;
        border-radius: 30px;
        width: 6rem;
        height: 2.8rem;
        text-align: center;
        margin: 0;
        margin-left: 1rem;
        line-height: 2.8rem;
    }

    .everydayBlock {
        background: #FFFFFF;
        border-radius: 12px;
        padding: 1.5rem;
        margin-top: 1.6rem;
    }
    .supplementTip {
        font-family: PingFang SC;
        font-style: normal;
        font-weight: normal;
        font-size: 1rem;
        margin-top: 3rem;
        color: #fff;
        text-align: center;
        letter-spacing: 1.5px;
        opacity: .9;
    }
</style>