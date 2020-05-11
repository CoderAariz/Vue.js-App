<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <br />
    <label for="t">Input</label>
    <br />
    <input type="text" name="I" id="I" placeholder="Enter Numeric Value" />
    <br />
    <input type="button" name="B" id="B" value="Cube" @click="handleClick" />
    <br />
    <span id="S">{{ message }}</span>
  </div>
</template>

<script const Vue="window.vue">
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  methods: {
    handleClick: function() {
      var n = document.getElementById("I").value;
      var pattern = /^[0-9]{1,}$/;
      if (pattern.test(n)) {
        document.getElementById("S").innerText = n * n * n;
      } else {
        alert("Enter only numeric value");
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hello label {
  color: white;
  font-family: "Times New Roman", Times, serif;
  font-size: 90%;
  font-weight: bold;
  position: absolute;
  margin: 20px 0px 0px 0px;
  left: 47%;
}

.hello input[type="text"] {
  width: 270px;
  height: 30px;
  color: rgb(122, 120, 120);
  background-color: whitesmoke;
  display: inline-block;
  position: absolute;
  margin: 35px 0px 16px 0px;
  font-size: large;
  padding: 20px;
  border: 5px solid rgb(104, 103, 103);
  border-radius: 30px;
  resize: vertical;
  box-sizing: border-box;
  text-align: center;
  left: 41%;
}
.hello input[type="button"] {
  background-color: rgb(255, 69, 0);
  color: white;
  text-align: center;
  font-size: 20px;
  padding: 10px 20px;
  border: none;
  position: relative;
  margin: 20px 0px 0px 0px;
  font-weight: bolder;
  cursor: pointer;
  border-radius: 5px;
  height: 35px;
  width: 250px;
  left: 1%;
  top: 30px;
  margin-bottom: 10px;
}

#S {
  width: 270px;
  height: 30px;
  font-family: "Times New Roman", Times, serif;
  color: rgb(122, 120, 120);
  background-color: whitesmoke;
  display: inline-block;
  position: relative;
  margin: 40px 0px 16px 0px;
  margin-bottom: 70px;
  font-size: large;
  padding: 25px;
  border: 5px solid rgb(104, 103, 103);
  border-radius: 30px;
  resize: vertical;
  box-sizing: border-box;
  text-align: center;
  left: 1%;
}
</style>
