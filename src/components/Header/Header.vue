<template>
  <header>
    <div class="container">
      <div class="header-info">
        <img class="header-img" src="../../assets/images/headre-img.jpg" alt="image">
        <div class="header-info__text">
          <div>
            <h1>Берлога програмиста</h1>
            <button @click="followBtn" :class=btnclass>{{ buttonValue }}</button>
          </div>
          <p>Ut sodales, ex sit amet consectetur accumsan, nibh ex sollicitudin metus, volutpat lacinia arcu nibh vel
            ante. Proin dapibus dui eget justo tincidunt eleifend. Mauris porta elementum est. Nullam euismod quis libero
            sed convallis. Vestibulum fringilla felis nec turpis aliquam auctor a a lectus. Etiam porttitor at eros vitae
            posuere. Suspendisse nec mollis dolor, vel cursus leo. Integer vitae sem vitae leo pretium porta. In consequat
            magna purus, iaculis rhoncus velit imperdiet sit amet.</p>
        </div>
      </div>

      <nav>
        <ul>
          <li>
            <router-link :to="{ path: '/' }" exact active-class="active">Публикации (124)</router-link>
          </li>
          <li>
            <router-link :to="{ path: '/kuzatuvchilar' }" exact active-class="active">Подписчики (124)</router-link>
          </li>
          <li>
            <router-link :to="{ path: '/xabarlar/1' }" exact active-class="active">Подробно o сообществе</router-link>
          </li>
        </ul>
      </nav>

      <div class="btn-group">
        <button class="btn-l">Опубликовать пост</button>
        <button class="btn-r"><svg width="15" height="15" viewBox="0 0 15 15" fill="none"
            xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd"
              d="M1.08325 7.49992C1.08325 11.0437 3.95609 13.9166 7.49992 13.9166C11.0437 13.9166 13.9166 11.0437 13.9166 7.49992C13.9166 3.95609 11.0437 1.08325 7.49992 1.08325C3.95609 1.08325 1.08325 3.95609 1.08325 7.49992ZM12.7499 7.49992C12.7499 10.3994 10.3994 12.7499 7.49992 12.7499C4.60042 12.7499 2.24992 10.3994 2.24992 7.49992C2.24992 4.60042 4.60042 2.24992 7.49992 2.24992C10.3994 2.24992 12.7499 4.60042 12.7499 7.49992ZM7.50011 10.4156C7.82238 10.4156 8.08363 10.1545 8.08363 9.83229C8.08363 9.51012 7.82238 9.24895 7.50011 9.24895C7.17784 9.24895 6.91658 9.51012 6.91658 9.83229C6.91658 10.1545 7.17784 10.4156 7.50011 10.4156ZM6.91658 8.66659H8.08325C8.08325 8.20088 8.15641 8.11552 8.63579 7.87583C9.46891 7.45927 9.83325 7.03421 9.83325 6.04159C9.83325 4.77029 8.83245 3.99992 7.49992 3.99992C6.21125 3.99992 5.16658 5.04459 5.16658 6.33325H6.33325C6.33325 5.68892 6.85559 5.16659 7.49992 5.16659C8.24493 5.16659 8.66658 5.49116 8.66658 6.04159C8.66658 6.50729 8.59342 6.59265 8.11404 6.83234C7.28092 7.2489 6.91658 7.67396 6.91658 8.66659Z"
              fill="#0066FF" />
          </svg>
          Задать вопрос в сообществе</button>
      </div>
    </div>
  </header>
</template>
<script>
import { RouterLink, } from 'vue-router';


export default {
  data() {
    return {
      buttonValue: 'Подписаться',
      btnclass: 'pod-btn',
    }

  },
  methods: {
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

  // mounted() {
  //   const oxirgiPath = this.$route.path;
  //   let li1 = document.querySelector('.li1')
  //   let li2 = document.querySelector('.li2')
  //   let li3 = document.querySelector('.li3')

  //   if (oxirgiPath == '/') {
  //     li2.classList.remove();
  //     li3.classList.remove();
  //     li1.classList.add('active')
  //   }
  //   if (oxirgiPath == '/kuzatuvchilar') {
  //     li1.classList.remove()
  //     li3.classList.remove()
  //     li2.classList.add('active')
  //   }
  //   if (oxirgiPath == '/xabarlar') {
  //     li2.classList.remove()
  //     li1.classList.remove()
  //     li3.classList.add('active')
  //   }
  //   console.log(oxirgiPath);

  //   return oxirgiPath;
  // }

}
</script>
<style scoped>
header {
  margin-bottom: 30px;
}

.header-info {
  position: relative;
  max-width: 920px;
  border-radius: 10px;
  background: var(--5, #FFF);
  margin: 0 auto;
  margin-top: 50px;
}

.header-info::before {
  content: '';
  position: absolute;
  background-image: url(../../assets/images/header-bf.png);
  top: 36%;
  left: 30px;
  /* bottom: 50%; */
  width: 92px;
  height: 92px;
}

.header-img {
  border-radius: 10px;
}

.header-info__text {
  padding: 58px 30px 34px;
}

.header-info__text div {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

h1 {
  color: var(--2, #1A1A1A);
  font-size: 22px;
  font-style: normal;
  font-weight: 600;
  line-height: 130%;
}

.pod-btn {
  padding: 10px 20px;
  align-items: center;
  border: none;
  border-radius: 10px;
  background: var(--1, #06F);
  color: var(--5, #FFF);
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
  cursor: pointer;
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
}

p {
  width: 585px;
  height: 80px;
  overflow: hidden;
  color: var(--3, #606060);
  text-overflow: ellipsis;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 140%;
}

nav ul {
  list-style: none;
  max-width: 920px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px;
  align-items: flex-start;
  border-radius: 10px;
  background: var(--11, #E5F0FF);
  margin: 10px auto 20px;
}

li {
  width: 300px;
  padding: 10px 20px;
  border-radius: 10px;
  background: var(--11, #E5F0FF);
  color: var(--1, #06F);
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
  text-align: center;
}

li a {
  color: currentColor;
  text-decoration: none;
}

.active {
  padding: 10px 50px;
  border-radius: 10px;
  background: var(--5, #FFF);
}


.btn-group {
  display: flex;
  width: 920px;
  padding: 10px;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
  border-radius: 10px;
  background: var(--5, #FFF);
  margin: 0 auto;
}

.btn-l {
  display: flex;
  height: 37px;
  padding: 10px 20px;
  justify-content: center;
  align-items: center;
  gap: 5px;
  flex: 1 0 0;
  border: none;
  border-radius: 10px;
  background: var(--1, #06F);
  border: 1px solid transparent;
  color: var(--5, #FFF);
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
  cursor: pointer;
  transition: all 0.5s ease;
}

.btn-l:hover {
  background: #fff;
  color: var(--1, #06F);
  border: 1px solid var(--1, #06F);
}

.btn-r {
  display: flex;
  height: 37px;
  padding: 10px 20px;
  justify-content: center;
  align-items: center;
  gap: 5px;
  flex: 1 0 0;
  border-radius: 10px;
  border: 1px solid var(--1, #06F);
  background: var(--5, #FFF);
  cursor: pointer;
  color: var(--1, #06F);
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
  transition: all 0.5s ease;
}

.btn-r:hover {
  background: var(--1, #06F);
  color: #fff;
  border: 1px solid var(--1, #06F);
}

.btn-r:hover svg path {
  fill: white;
}

path {
  transition: all 0.5s ease;
}
</style>