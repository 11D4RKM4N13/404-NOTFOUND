<template>
  <div class="content">
    
    <p>
      OPPSS! PAGE NOT FOUND!
    </p>

    <div class="notfound">
      <h2>404</h2>
      <h2>404</h2>
    </div>

    <div class="Button">
      <a href="#">
        {{Button}}
      </a>
    </div>
    
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      Titulo: 'OPPS! LOOKS LIKE YOU ARE LOST!',
      Button: 'GO BACK'
    }
  }
}
</script>

<style>

/*Imports*/
@import url('https://fonts.googleapis.com/css2?family=Orbitron&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Frijole&display=swap');

*{
  margin: 0%;
  padding: 0%;
  box-sizing: border-box;
  /*font-family: 'Orbitron', sans-serif;*/
  font-family: 'Frijole', cursive;
}

body{
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-image: url("assets/deepsea.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}

.notfound{
  position: relative;
}

.notfound h2{
  position: absolute;
  /*color: #ffff;*/
  transform: translate(-50%, -50%);
  font-size: 8em;
}

.notfound h2:nth-child(1){
  color: transparent;
  -webkit-text-stroke: 2px #03a9f4;
}

.notfound h2:nth-child(2){
  color: #03a9f4;
  animation: animate 2s ease-in-out infinite;
}

@keyframes animate {
  0%, 100%{
    clip-path: polygon(
      0% 45%, 15% 44%, 32% 50%,
      54% 60%, 70% 61%, 84% 59%, 100% 52%,
      100% 100%, 0% 100%
    );
  }
  50%{
    clip-path: polygon(
      0 60%, 16% 65%, 34% 66%, 51% 62%,
      67% 50%, 84% 45%, 100% 46%, 100% 100%, 0% 100%      
    );
  }
}

.content .Button{
  position: absolute;
  bottom: 5%;
  left: 43.5%;
}

.content .Button a{
  position: relative;
  display: inline-block;
  padding: 15px 30px;
  color: #2196f3;
  text-transform: uppercase;
  letter-spacing: 4px;
  text-decoration: none;
  font-size: 25px;
  overflow: hidden;
  transition: 0.2s;
}

.content .Button a:hover{
  color: #255784;
  background: #2196f3;
  box-shadow: 0 0 10px #2196f3, 0 0 40px #2196f3, 0 0 80px #2196f3;
}

.content p{
  position: absolute;
  top: 60%;
  left: 35%;
  color: #03a9f4;
  font-size: 30px;
}

</style>