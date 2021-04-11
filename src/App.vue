<template>
  <div class="notfound">
    <h2>404</h2>
    <h2>404</h2>
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      Titulo: 'OPPS! LOOKS LIKE YOU ARE LOST!'
    }
  }
}
</script>

<style>

/*Imports*/
@import url('https://fonts.googleapis.com/css2?family=Orbitron&display=swap');

*{
  margin: 0%;
  padding: 0%;
  box-sizing: border-box;
  font-family: 'Orbitron', sans-serif;
}

body{
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: black;
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

</style>