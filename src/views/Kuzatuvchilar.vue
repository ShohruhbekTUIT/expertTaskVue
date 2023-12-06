<template>
  <main>
    <div class="container">
      <ul class="people-list">
        <Person v-for="item in o = people" :datas="item" />
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
import Person from '../components/Person/Person.vue';
export default {
  data() {
    return {
      people: [
        {
          id: 1,
          img: './src/assets/images/RiskySmith.png',
          name: 'Ricky Smith',
          city: 'Ташкент',
        },
        {
          id: 2,
          img: './src/assets/images/KurtBates.png',
          name: 'Kurt Bates',
          city: 'Ташкент',
        },
        {
          id: 3,
          img: './src/assets/images/JoshuaJones.png',
          name: 'Joshua Jones',
          city: 'Ташкент',
        },
        {
          id: 4,
          img: './src/assets/images/IvaRyan.png',
          name: 'Iva Ryan',
          city: 'Ташкент',
        },
        {
          id: 5,
          img: './src/assets/images/KathyPacheco.png',
          name: 'Kathy Pacheco',
          city: 'Ташкент',
        },
        {
          id: 6,
          img: './src/assets/images/Stephanie.png',
          name: 'Stephanie Nicol',
          city: 'Ташкент',
        },
        {
          id: 7,
          img: './src/assets/images/Corina.png',
          name: 'Corina McCoy',
          city: 'Ташкент',
        },
        {
          id: 8,
          img: './src/assets/images/Rodger.png',
          name: 'Rodger Struck',
          city: 'Ташкент',
        },
        {
          id: 9,
          img: './src/assets/images/Chris.png',
          name: 'Chris Glasser',
          city: 'Ташкент',
        },
      ]
    };
  },
  components: { Person },

}



</script>
<style>
h1 {
  text-align: center;
}

.people-list {
  width: 920px;
  list-style: none;
  margin: 0 auto 30px;
  padding: 0;
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