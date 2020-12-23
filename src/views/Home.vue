<template>
  <div class="home">
    <section>
      <Teste :title="title" :show="show" :description="description" :description2="description2" />
      <Teste :title="title" :show="show" :description="description" :description2="description2" />
    </section>
    <section>
      <Teste :title="title" :show="show" :description="description" :description2="description2"/>
      <Teste :title="title" :show="show" :description="description" :description2="description2"/>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import Teste from '@/components/Teste.vue'

export default {
  name: 'Home',
  data(){
    return {
      show: true,
      title: "Lorem",
      description: "Lorem",
      description2: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus nec diam fermentum, elementum enim non, molestie nisl. Duis malesuada erat diam, accumsan ultricies tellus faucibus non. Pellentesque aliquam dui id lobortis pulvinar. Nullam sit amet lacus non augue ultricies auctor id molestie tortor. Duis nulla eros, fermentum vitae lacus id, finibus scelerisque nulla. Ut in sem ligula. Aenean vitae pulvinar libero. In molestie, libero posuere mollis dapibus, velit dolor placerat ante, et pellentesque neque est lobortis magna. Donec imperdiet nunc vel mi tempus lacinia. Nam dapibus fringilla auctor. Fusce scelerisque ex vel sodales venenatis. Donec a lacus arcu.",
    }
  },
  components: {
    Teste
  }
}
</script>

<style scoped>
  .home {
    display: flex;
    justify-content: space-around;
    min-height: 500px;
  }
</style>