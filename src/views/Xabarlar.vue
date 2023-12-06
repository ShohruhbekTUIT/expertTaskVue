<template>
  <main>
    <div class="container">
      <div class="xabarlar">
        <div class="user-data">
          <div class="user-data-info">
            <h2>Автор сообщества</h2>
            <Person :datas="people[$route.params.id - 1]" />
          </div>
        </div>
        <div>
          <h3 class="xabar-title">
            O сообществе
          </h3>
          <p class="xabar-text">
            Ut sodales, ex sit amet consectetur accumsan, nibh ex sollicitudin metus, volutpat lacinia arcu nibh vel ante.
            Proin dapibus dui eget justo tincidunt eleifend. Mauris porta elementum est. Nullam euismod quis libero sed
            convallis. Vestibulum fringilla felis nec turpis aliquam auctor a a lectus. Etiam porttitor at eros vitae
            posuere. Suspendisse nec mollis dolor, vel cursus leo. Integer vitae sem vitae leo pretium porta. In consequat
            magna purus, iaculis rhoncus velit imperdiet sit amet. Ut sodales, ex sit amet consectetur accumsan, nibh ex
            sollicitudin metus, volutpat lacinia arcu nibh vel ante. Proin dapibus dui eget justo tincidunt eleifend.
            Mauris porta elementum est. Nullam euismod quis libero sed convallis. Vestibulum fringilla felis nec turpis
            aliquam auctor a a lectus. Etiam porttitor at eros vitae posuere. Suspendisse nec mollis dolor, vel cursus
            leo. Integer vitae sem vitae leo pretium porta. In consequat magna purus, iaculis rhoncus velit imperdiet sit
            amet.
          </p>
        </div>
      </div>
    </div>
  </main>
</template>
<script>
import Person from '../components/Person/Person.vue';



export default {
  components: { Person },
  data() {
    return {
      people: [
        {
          id: 1,
          img: '../src/assets/images/RiskySmith.png',
          name: 'Ricky Smith',
          city: 'Ташкент',
        },
        {
          id: 2,
          img: '../src/assets/images/KurtBates.png',
          name: 'Kurt Bates',
          city: 'Ташкент',
        },
        {
          id: 3,
          img: '../src/assets/images/JoshuaJones.png',
          name: 'Joshua Jones',
          city: 'Ташкент',
        },
        {
          id: 4,
          img: '../src/assets/images/IvaRyan.png',
          name: 'Iva Ryan',
          city: 'Ташкент',
        },
        {
          id: 5,
          img: '../src/assets/images/KathyPacheco.png',
          name: 'Kathy Pacheco',
          city: 'Ташкент',
        },
        {
          id: 6,
          img: '../src/assets/images/Stephanie.png',
          name: 'Stephanie Nicol',
          city: 'Ташкент',
        },
        {
          id: 7,
          img: '../src/assets/images/Corina.png',
          name: 'Corina McCoy',
          city: 'Ташкент',
        },
        {
          id: 8,
          img: '../src/assets/images/Rodger.png',
          name: 'Rodger Struck',
          city: 'Ташкент',
        },
        {
          id: 9,
          img: '../src/assets/images/Chris.png',
          name: 'Chris Glasser',
          city: 'Ташкент',
        },
      ]
    };
  },
  methods: {

  },
}
</script>
<style scoped>
.xabarlar {
  width: 920px;
  margin: 0 auto;
  border-radius: 10px;
  background: var(--5, #FFF);
  padding: 30px 20px;
  margin-bottom: 45px;
}

.user-data {
  padding-bottom: 25px;
  border-bottom: 1px solid #F3F3F3;
}

.user-data-info {
  max-width: 340px;
}

h2 {
  color: var(--2, #1A1A1A);
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 120%;
}

.xabar-title {
  color: var(--2, #1A1A1A);
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 120%;
  margin-bottom: 15px;
}

.xabar-text {
  color: var(--3, #606060);
  text-align: justify;
  /* text-overflow: ellipsis; */
  /* white-space: nowrap; */
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 140%;
}
</style>