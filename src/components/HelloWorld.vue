<template>
  <div class="row">
    <div class="col-lg-6" id="firsthalf">
      <h1 id="name">{{ person.name }}</h1>
      <div class="firsthalfnav">
        <h3>home</h3>
        <h3>about</h3>
      </div>
    </div>
    <div class="image-container">
      <img src="../assets/girl.png" alt="girl image" />
    </div>
<div class="circleimage">
  <img src="../assets/black.jpg" alt="girl image" />
</div>
    <div class="col-lg-6" id="secondhalf">
      <div class="secondhalfnav">
        <h3>gallery</h3>
        <h3>contact</h3>
      </div>
      <div class="icon-bar">
        <a
         
          class="facebook"
          ><i class="fa fa-instagram"></i
        ></a>
        <a href="#" class="twitter"><i class="fa fa-twitter"></i></a>
        <a href="#" class="google"><i class="fa fa-snapchat"></i></a>
        <a href="#" class="linkedin"><i class="fa fa-envelope"></i></a>
      </div>
    </div>
  </div>
</template>
//  :href="`/instagram.com/${person.social_media.instagram}`"
<script>
export default {
  methods: {},
  data() {
    return {
      person: "",
    };
  },
  mounted() {
    fetch("https://hirng-x2021.glitch.me/api")
      .then((response) => response.json())
      .then((data) => (this.person = data));
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  overflow-x: hidden;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: 100;
  color: #ffffff;
  overflow: hidden;
}
#name {
  letter-spacing: 1rem;
  position: absolute;
  left: 33%;
}
#firsthalf,
#secondhalf {
  height: 100vh;
}
#firsthalf {
  background-color: #bd0f4d;
}
#secondhalf {
  background-color: #cb2964;
}
.firsthalfnav {
  display: flex;
  position: absolute;
  bottom: 10px;
  left: 200px;
}
.secondhalfnav {
  display: flex;
  position: absolute;
  bottom: 10px;
  right: 200px;
}
.firsthalfnav h3,
.secondhalfnav h3 {
  text-transform: uppercase;
  font-size: 20px;
}
.firsthalfnav h3,
.secondhalfnav h3 {
  margin-left: 50px;
}
.image-container {
  width: 500px;
  height: 500px;
  background-color: #ca2b65;
  position: absolute;
  left: 33%;
  top: 10%;
  overflow: hidden;
  -webkit-box-shadow: -4px 10px 37px -12px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: -4px 10px 37px -12px rgba(0, 0, 0, 0.75);
  box-shadow: -4px 10px 37px -12px rgba(0, 0, 0, 0.75);
}
.image-container img {
  position: relative;
  top: -68px;
  height: 700px;
  right: 55%;
}
.circleimage{
  position: absolute;
  width:80px;
  height: 80px;
  border:1px solid white;
  border-radius: 50%;
  bottom: 0;
  left: 47%;
  background-image: url('../assets/black.jpg');
  background-position: center;
}
.icon-bar {
  position: fixed;
  top: 50%;
  right: 10px;
  -webkit-transform: translateY(-50%);
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}

.icon-bar a {
  display: block;
  text-align: center;
  padding: 16px;
  transition: all 0.3s ease;
  color: white;
  font-size: 40px;
}
</style>
