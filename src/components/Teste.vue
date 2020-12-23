<template>
  <div class="teste">
    <section class="title">
      <h3>{{title}}</h3>
    </section>
    <section class="paragraph" @mouseenter="mudaShow()" @mouseleave="mudaShow()">
      <p v-show="show">{{description}}</p>
      <p v-show="!show">{{description2}}</p>
    </section>
  </div>
</template>

<script>

export default {
  name: 'Teste',
  props: {
    show: Boolean,
    title: String,
    description: String,
    description2: String,
  },
  methods: {
    mudaShow: function(){
      this.show = !(this.show);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  p {
    overflow: auto;
    text-align: center;
  }
  p:hover {
    text-align: justify;
  }
  h3, p{
    padding: 10px;
    margin: 0px;
  }
  section {
    border-radius: 30px;
  }
  .teste {
    border: solid 3px rgba(92, 183, 248, 97);
    width: 150px;
    margin-bottom: 2%;
    border-radius: 10px;
    background: rgba(92, 183, 248, 97);
    margin-top: 50px;
  }
  .title {
    text-align: center;
    min-height: 50px;
    background-color: rgba(92, 183, 248, 97);
  }
  .paragraph {
    background-color: rgba(92, 248, 141, 97);
    transition: 1s;
    box-sizing: border-box;
    margin-bottom: 10px;
    overflow: auto;
  }
  .paragraph:hover {
    height: 400px;
    transition: 1s ;
  }
</style>
