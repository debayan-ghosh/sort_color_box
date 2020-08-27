<template>
  <div id="app" class="boxdisplay">
    <h1>Shuffle and Sort</h1>
    <div class="container">
      <div id="first">
        <button class="button" @click="shuffleElements">SHUFFLE</button>
        <br />
        <br />
        <button class="button" @click="sortElements">SORT</button>
      </div>
      <div id="second">
        <div :class="row" v-for="value in myArr" :key="value.number">
          <div class="column" :style="{ backgroundColor: `${value.color}` }">
            <h2 class="numbers">{{value.number}}</h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NumberBox",
  data() {
    return {
      myArr: [
        {
          number: 1,
          color: "#000000",
        },
        {
          number: 2,
          color: "#333333",
        },
        {
          number: 3,
          color: "#FFFFFF",
        },
        {
          number: 4,
          color: "#EFEFEF",
        },
        {
          number: 5,
          color: "#72C3DC",
        },
        {
          number: 6,
          color: "#2B8EAD",
        },
        {
          number: 7,
          color: "#6F98A8",
        },
        {
          number: 8,
          color: "#BFBFBF",
        },
        {
          number: 9,
          color: "#2F454E",
        },
      ],
    };
  },
  methods: {
    shuffleElements: function () {
      return this.myArr.sort(() => Math.random() - 0.5);
    },
    sortElements: function () {
      return this.myArr.sort((a, b) => a.number - b.number);
    },
  },
  mounted() {},
};
</script>

<style scoped>
.column {
  float: left;
  width: 33.33%;
}

.column {
  float: left;
  border: 1px;
}

.button {
  background-color: #659ec7;
  border-radius: 14px;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.container {
  width: 100%;
  margin: auto;
}
.numbers {
  color: white;
  text-shadow: 1px 0px #000000;
  height: 50px;
}
#first {
  width: 50%;
  float: right;
  height: 300px;
}
#second {
  width: 50%;
  float: left;
  height: 300px;
}
@media (max-width: 375px) { 
#first {
  width: 50%;
  float: right;
  height: 300px;
}
#second {
  width: 50%;
  float: left;
  height: 300px;
}
}
</style>


