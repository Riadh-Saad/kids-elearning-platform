<template>
  <header>
    <nav>
      <input type="checkbox" id="check" />

      <i class="fas fa-bars"></i>

      <label class="logo">Responsive Nav</label>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Feedback</a></li>
      </ul>
    </nav>
    <div class="bg"></div>
  </header>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
  text-decoration: none;
  list-style: none;
  box-sizing: border-box;
}
body {
  font-family: monospace;
}
nav {
  background-color: rgb(73, 4, 138);
  height: 80px;
  width: 100%;
}
label.logo {
  color: white;
  font-size: 35px;
  line-height: 80px;
  padding: 0 100px;
  font-weight: bold;
}
nav ul {
  float: right;
  margin-right: 100px;
}
nav ul li {
  display: inline-block;
  line-height: 80px;
  margin: 0 5px;
}
nav ul li a {
  color: white;
  font-size: 22px;
  text-transform: uppercase;
  padding: 5px 10px;
}
nav ul li a.active,
nav ul li a:hover {
  background: #1b9bff;
  transition: 0.5s;
  border-radius: 5px;
}
.checkbtn {
  float: right;
  color: white;
  margin-right: 40px;
  display: none;
  cursor: pointer;
}
.checkbtn i {
  line-height: 80px;
  font-size: 25px;
}
#check {
  display: none;
}
@media (max-width: 950px) {
  label.logo {
    font-size: 30px;
    padding-left: 50px;
  }
  nav ul li a {
    font-size: 18px;
  }
}
@media (max-width: 858px) {
  .checkbtn {
    display: block;
  }
  nav ul {
    position: fixed;
    width: 100%;
    height: 100vh;
    background: #2c3e50;
    top: 80px;
    left: -100%;
    transition: all 0.5s;
    text-align: center;
  }
  nav ul li {
    display: block;
    margin: 70x 0;
    line-height: 50px;
  }
  nav ul li a {
    font-size: 22px;
  }
  a:hover,
  a.active {
    background: none !important;
    color: #0082e6;
  }
  #check:checked ~ ul {
    left: 0;
  }
}
.bg {
  background: url("https://images.pexels.com/photos/1410225/pexels-photo-1410225.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940")
    no-repeat;
  background-size: cover;
  width: 100%;
  height: 100%;
}
</style>
