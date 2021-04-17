  
<template>
  <body>
  
  <div id="app">
    <nav class="main-nav">
  
       <!-- <img src="../src/assets/leave.png" alt="Ohhh Canada">    -->
       
          <ul class="topnav">
            <li><a class="active" href="#home">Home</a></li>
            <li><a href="#news">News</a></li>
            <li><a href="#contact">Contact</a></li>
            <!-- <p>hi<p> -->
            <li class="right"><a href="#about">About</a></li>
          </ul>
      
       </nav>
        <section class="main">
        <h3>COVID-19 Canada Dashboard</h3>
     

      <graphs>
        <p> {{posts}} </p>
      </graphs>
   
   </section>

 
 <footer> All Data Taken from Covid 19 .org </footer>
  </div>

  </body>
</template>

<script>

import graphs from "./components/graphs.vue";


export default {
  name: "app",
  components: {
    graphs
  }
};
</script>
<style>
html {
  height: 100%;
  overflow: hidden;
}
body {
  border: 0;
  margin: 0;
  padding: 0;
  font-family: Gill Sans Extrabold, sans-serif;
  height: 100%;
  background: rgb(101, 31, 87);
  background:#f6f6f6;
}
.logo {
  align-self: center;
  color: #fff;
  font-weight: bold;
  font-family: Gill Sans Extrabold, sans-serif;
  text-align: center;
  font-size: 59px;
  flex-direction: row;   
  align-items: baseline; 
 
  

  height:100px;

}

.main-nav {
  /* display: block; */
  border: 0px solid red;
  align-items: center;
  /* display:flex; */
  padding-top: 4px;
   font-family: Gill Sans Extrabold, sans-serif;
  background-color: #deeaee;
 
}

img
{
  width: 6%;
  height: 100%;
  object-fit: contain;
  margin: 13px;
}

ul.topnav {
  list-style-type: none;
  margin: 0;
  padding: 0;
  height: 46px;
  background-color:#eea29a;
  overflow:hidden;
}

ul.topnav li{float: left;
background-color:#eea29a;}
/* all of them are li a */
ul.topnav li a{
  display:block;
  color:white;
  text-align: center;
  padding: 14px 14px;
  text-decoration:none;
  margin: 0px;
  }

ul.topnav p{
  float:left;


}

ul.topnav li a:hover:not(.active) {background-color: rgb(211, 91, 91);}
ul.topnav li a.active {background-color: #b1cbbb;
float: left;
}
ul.topnav li.right {float: right;
}


@media screen and (max-width: 300px) {
  ul.topnav li.right, 
  ul.topnav li {float: none;}
}


/* #app{

  display: grid;
  grid-template: auto 1fr auto;


} */

footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;

  background-color: #deeaee;
  color: #c94c4c;
  text-align:center;
  -moz-text-size-adjust: auto;
}

section.main{
  display:flexbox;

}

section.main h3{
  text-align: center;
}

</style>