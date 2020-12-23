<template>
  <div id="app">
    <div id="nav">
      <div id="corpoHeader">
        <div class="inLine"><router-link to="/" class="linksHeader linksRoots">Home</router-link></div>
        <div class="inLine" @mouseover="loginOn = true" >
          <router-link to="/login" class="linksHeader linksRoots" id="login">Login</router-link> 
        </div>
        <div class="inLine"><router-link to="/about" class="linksHeader linksRoots">About</router-link> </div>
      </div>
      <div @mouseleave="loginOn = false">
        <section v-show="loginOn" id="aparecer">
          <router-link to="/activies" v-show="loginOn" class="linksHeader subDivisoes">Activies</router-link>
          <router-link to="/photos" v-show="loginOn" class="linksHeader subDivisoes">photos</router-link> 
        </section>
      </div>
    </div>
    <router-view/>
    <footer id="footer">
      <a href="https://github.com/Epilef1177" target="_blank" rel="noopener noreferrer">GitHub</a>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      loginOn: false,
    }
  },
  component: {
  },
  methods: {
  }
}
</script>

<style>
footer a {
  color: rgba(240, 144, 101, 94);
  text-decoration: none;
  font-size: 20pt;
  margin: 30px auto 0px auto;
  transition: 1s;
}
footer a:hover {
  color: rgba(133, 255, 241, 100);
  transition: 1s;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin: -9px auto auto auto;
  width: 90%;
  background-color: rgba(133, 255, 241, 100);
}
#nav {
  display: block;
  max-height: 100px;
  min-height: 90px;
}
.inLine{
  display: inline-block;
  margin-top: 20px;
}
.linksHeader {
  margin: 0px 30px 0px 30px ;
  padding: 5px;
  border: 1px solid rgba(240, 144, 101, 94);;
  border-radius: 10px;
  max-width: 100px;
  min-width: 60px;
  color: rgba(240, 144, 101, 94);
  text-decoration: none;
  font-size: 30pt;
}
.linksRoots {
  transition: 1s;
}
.linksRoots:hover {
  background-color: rgba(163, 75, 36, 64);
  transition: 1s;
}
#corpoHeader{
  max-height: 200px;
  min-height: 100px;
  background: rgba(52, 163, 150, 64); 
}
#aparecer {
  margin-top: -30px;
  padding: 10px;
  max-height: 150px;
  min-height: 40px;
  display: inline-block;
  border-radius: 50px;
  background: rgba(163, 75, 36, 64);
}
.subDivisoes {
  transition: 1s;
}
.subDivisoes:hover {
  background-color: rgba(133, 255, 241, 100);
  transition: 1s;
}
#footer {
  
  height: 100px;
  background-color: rgba(163, 75, 36, 64);
  padding: 20px;
}
 /** 
* {
  azul escuro   background-color: rgba(52, 163, 150, 64);
  azul claro    background-color: rgba(133, 255, 241, 100);
  azul médio    background-color: rgba(100, 240, 224, 94);
  marrom        background-color: rgba(163, 75, 36, 64);
  marrom claro  background-color: rgba(240, 144, 101, 94);

  azul marinho      background-color: rgba(92, 183, 248, 97);
  azul esverdeadeo  background-color: rgba(80, 196, 217, 85);
  azul bebê         background-color: rgba(100, 240, 224, 94);
  verde mato        background-color: rgba(80, 217, 162, 85);
  verde claro       background-color: rgba(92, 248, 141, 97);
}
*/
</style>
