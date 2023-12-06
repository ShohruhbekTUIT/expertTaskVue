<template>
  <li :data-Id="datas.id" @click="userComment">
    <img :src=datas.img alt="avatar">
    <div>
      <strong>{{ datas.name }}</strong>
      <span>{{ datas.city }}</span>
    </div>
    <button @click="followBtn" :class=btnclass>{{ buttonValue }}</button>
  </li>
</template>
<script>
import { } from 'vue-router';

export default {
  props: {
    datas: {
      type: Object,
      required: true,
    }
  },
  data() {
    return {
      buttonValue: 'Подписаться',
      btnclass: 'pod-btn',
    }
  },
  methods: {
    userComment() {
      this.$router.push('/xabarlar/' + this.datas.id);
      // console.log(this.datas.id);
    },
    followBtn() {
      // console.log(this.$data.valueOf());
      // let i = 0;
      // if (i == 0) {
      //   ++i;
      //   return { clas: 'pod-btn', text: 'Подписаться', }
      // }
      // if (i == 1) {
      //   --i;
      //   return { clas: 'odps-btn', text: 'Отписаться', }
      // }
      if (this.buttonValue == 'Отписаться') {
        this.buttonValue = 'Подписаться';
        this.btnclass = 'pod-btn';
        return
      }
      if (this.buttonValue == 'Подписаться') {
        this.buttonValue = 'Отписаться';
        this.btnclass = 'odps-btn';
      }
    }
  }
}
</script>
<style scoped>
li {
  display: flex;
  align-items: center;
  padding: 10px 20px;
  border-radius: 10px;
  background: var(--5, #FFF);
  margin-bottom: 15px;
}

img {
  margin-right: 10px;
}

div {
  display: flex;
  flex-direction: column;
}

strong {
  margin-bottom: 5px;
  color: var(--2, #1A1A1A);
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
}

span {
  color: var(--3, #606060);
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 140%;
}

.pod-btn {
  padding: 10px 20px;
  border-radius: 10px;
  background: var(--1, #06F);
  border: 1px solid transparent;
  color: var(--5, #FFF);
  font-size: 12px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
  margin-left: auto;
  transition: all .2s ease;
}

button:hover {
  opacity: 0.7;
}

.odps-btn {
  padding: 10px 20px;
  align-items: center;
  border: none;
  border-radius: 10px;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
  border: 1px solid var(--4, #F3F3F3);
  background: var(--4, #F3F3F3);
  cursor: pointer;
  margin-left: auto;
}
</style>