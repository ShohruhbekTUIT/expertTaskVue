<template>
  <main>
    <div class="container">
      <ul class="posts">
        <Post v-for="post in posts" :datas="post" />
      </ul>
      <button class="more-btn">Показать еще (12 342)
        <svg width="19" height="19" viewBox="0 0 19 19" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" clip-rule="evenodd"
            d="M14.9697 5.96973L16.0304 7.03039L9.50006 13.5607L2.96973 7.03039L4.03039 5.96973L9.50006 11.4394L14.9697 5.96973Z"
            fill="white" />
        </svg>

      </button>
    </div>
  </main>
</template>
<script>
import Post from '../components/Post/Post.vue';

export default {
  components: { Post },
  data() {
    return {
      posts: [
        {
          avatar: './src/assets/images/Eddie.png',
          name: 'Eddie Lake',
          link: 'Вопрос-ответ',
          title: 'День 478: россияне лидируют среди иностранных покупателей недвижимости в Турции',
          text: '«Азбука вкуса» начала производство готовой еды для российских авиакомпаний «Россия» и «Смартавиа», пишут «Ведомости». На этапе тестов блюда стали доступны пассажирам, вылетающим из аэропортов «Шереметьево» и «Пулково».',
          pic: './src/assets/images/Eddie-post-img.png',
        },
        {
          avatar: './src/assets/images/Rhonda.png',
          name: 'Rhonda Rhodes',
          link: 'Обсуждение',
          title: 'День 478: россияне лидируют среди иностранных покупателей недвижимости в Турции',
          text: '«Азбука вкуса» начала производство готовой еды для российских авиакомпаний «Россия» и «Смартавиа», пишут «Ведомости». На этапе тестов блюда стали доступны пассажирам, вылетающим из аэропортов «Шереметьево» и «Пулково».',
          pic: './src/assets/images/Rhonda-post-img.png',
        },
        {
          avatar: './src/assets/images/David.png',
          name: 'David Elson',
          link: 'Пост',
          title: 'День 478: россияне лидируют среди иностранных покупателей недвижимости в Турции',
          text: '«Азбука вкуса» начала производство готовой еды для российских авиакомпаний «Россия» и «Смартавиа», пишут «Ведомости». На этапе тестов блюда стали доступны пассажирам, вылетающим из аэропортов «Шереметьево» и «Пулково».',
          pic: './src/assets/images/David-post-img.png',
        },
      ]
    }
  }
}
</script>
<style scoped>
.posts {
  max-width: 920px;
  list-style: none;
  display: flex;
  flex-direction: column;
  padding: 0;
  margin: 0 auto;
}

.more-btn {
  display: flex;
  height: 39px;
  padding: 10px 20px;
  align-items: center;
  gap: 5px;
  border-radius: 10px;
  background: var(--1, #06F);
  color: var(--5, #FFF);
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 120%;
  border: none;
  cursor: pointer;
  margin: 0 auto 50px;
  transition: all 0.5s ease;
}

.more-btn:hover {
  opacity: 0.6;
}
</style>