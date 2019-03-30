<template>
  <article>
    <Slider :items="items" :cname="$style.slide"/>
    <section :class="$style.list">
      <div :class="$style.item" v-for="item in enters" :key="item.img">
        <router-link :to="{name: item.href}">
          <img :src="item.img" :alt="item.title">
          <h4>{{item.title}}</h4>
        </router-link>
      </div>
    </section>
  </article>
</template>

<script>
  import Slider from "../core/slider";

  export default {
    name: "hslider",
    components: {
      Slider
    },
    data () {
      return {
        items: [
          {
            src: 'https://img12.360buyimg.com/jrpmobile/jfs/t1/28576/40/10399/139307/5c862bc6E022a873e/c50fcefa58db30ce.jpg',
            href: 'home1'
          },
          {
            src: 'https://img12.360buyimg.com/jrpmobile/jfs/t1/10297/24/14008/46685/5c862b47Eef810b58/30b8c5430103352a.jpg',
            href: 'home2'
          },
          {
            src: 'https://img12.360buyimg.com/jrpmobile/jfs/t1/19037/8/10380/37518/5c862ba2Ec8e629f7/6c4f8c721cf210d8.jpg',
            href: 'home3'
          }
        ],
        enters: [
          {
            href: 'home',
            img: 'https://img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png',
            title: '优惠券'
          },
          {
            href: 'home',
            img: 'https://img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png',
            title: '领福利'
          },
          {
            href: 'home',
            img: 'https://img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png',
            title: '抢钢镚'
          },
          {
            href: 'home',
            img: 'https://img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png',
            title: '白条提额'
          },
          {
            href: 'home',
            img: 'https://img12.360buyimg.com/jrpmobile/jfs/t1/520/34/950/3686/5b9239e3Eaaf5465c/8d8c35badacfc114.png',
            title: '工资理财'
          }
        ]
      }
    }
  }
</script>

<style lang="scss" module>
@import "../../css/element";
  .slide {
    margin-top: 120px;
    img {
      width: 100%;
    }
  }
  .list {
    @include list(row);
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around;
    background-color: #fff;
    a {
      text-decoration: none;
    }
    .item {
      text-align: center;
      img {
        display: inline-block;
        width: 110px;
        height: 110px;
      }
      h4 {
        font-size: 26px;
        margin-top: 12px;
        color: #666;
      }
    }
  }
</style>
