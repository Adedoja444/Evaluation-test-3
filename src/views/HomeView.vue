<template>
  <div class="container">
    <div class="staff">
      <div class="card" v-for="person in persons" :key="person.id">
        <ul>
          <li>Name:{{ person.name }}</li>
          <li>Gender:{{ person.gender }}</li>
          <li>Role:{{ person.role }}</li>
          <li>Complexion:{{ person.complexion }}</li>
        </ul>
      </div>
    </div>
    <div>
      <p class="number">{{count}}</p>
      <button @click="count--">Decrease Count</button>
      <button @click="increment">Increase Count</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {

       count: 0,
       text: 'I am learning about Vue',
       persons: [
        {
          id: "1",
          name: "Henry",
          gender: "Male",
          role: "Tutor",
          complexion: "light-skinned",
        },
        {
          id: "2",
          name: "Ray",
          gender: "Male",
          role: "Tutor",
          complexion: "light-skinned",
        },
        {
          id: "3",
          name: "Max",
          gender: "Male",
          role: "Tutor",
          complexion: "light-skinned",
        },
        {
          id: "4",
          name: "Charlotte",
          gender: "Female",
          role: "Tutor",
          complexion: "Dark",
        },
        {
          id: "5",
          name: "Phoebe",
          gender: "Female",
          role: "Secretary",
          complexion: "light-skinned",
        },
        {
          id: "6",
          name: "Trip",
          gender: "Male",
          role: "Tutor",
          complexion: "Dark",
        },
        {
          id: "7",
          name: "Cherry",
          gender: "Female",
          role: "Cleaner",
          complexion: "light-skinned",
        },
      ],
     
    };
  },
  methods: {
      increment() {
        this.count++
        if(this.count < 10) {
          document.querySelector('number').classList.add('green')
        } else {
          document.querySelector('number').classList.add('red')
        }
      },
  }
};
</script>

<style scoped>
.container {
   width: 90%;
}

.staff {
   display: flex;
   justify-content: left;
   flex-wrap: wrap;
}

.card {
  width: 20%;
  border-radius: 5px;
  /* height: 30vh; */
  background-color: rgb(240, 240, 240);
  color: #000;
  padding: 20px 0;
  margin: 2px 4px;
  text-align: left;
  font-size: 15px;
}

ul li {
  list-style-type: none;
}

li {
  padding-top: 2px;
}

.green {
  color: green;
}

.red {
  color: red;
}

</style>


