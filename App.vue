<template>
  <div class="container">
    <br> <br>
    <button @click="selectedComponent='appMemory'" class="btn-sm btn btn-primary">appMemory</button>
    <button @click="selectedComponent='appNewMemory'" class="btn-sm btn btn-primary">appNewMemory</button>
    <button  @click="selectedComponent='appAuthor'" class="btn-sm btn btn-primary">appAuthor</button>
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <hr>
        <p> {{ selectedComponent }}</p>
        <hr>

        <!-- is attribute ı buraya ait bir component varsa onu burada göstermeyi sağlıyor-->
        <!-- keep-alive sayesinde componentlerin tekrar render edilmesini engelliyoruz. dolayısıyla destroy olmuyor-->

        <KeepAlive>
          <component :is="selectedComponent">
            <h3 slot="heading">It's a good day..</h3>
            <p>It was great memory</p>
          </component>
        </KeepAlive>
       

      </div>
    </div>
  </div>
</template>

<!--content(içerik) gönderme
content: p,h1,pic gibi elementler icerir -->
<!-- slot ile içerik göndermek -->
<!-- named slot ile contentleri ayrıştırmak  -->
<!-- default slot ve slot defaults-->

<script>
import Memory from './components/memory.vue'
import Author from './components/Author.vue'
import NewMemory from './components/NewMemory.vue'


export default {
  data : function() {
      return {
        selectedComponent : "appMemory"
      }
  },
  components: {
    'appMemory': Memory,
    'appAuthor': Author,
    'appNewMemory': NewMemory
  }
}
</script>


