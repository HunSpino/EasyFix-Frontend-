<template>
  <div class="card" style="width: 18rem;">
    <img src="" class="card-img-top" alt="...">
    <div class="card-body">
        <h5 class="card-title"> . Gép</h5>
        <p class="card-text">Épület: </p>
        <p class="card-text">Emelet: </p>
        <p class="card-text">Terem: </p>
        <p class="card-text">Gép: </p>
    </div>
  </div>
    
</template>

<script>
export default {
    name: 'GepekList',
  components: {
  },
  data() {
    return {
      mod_new: true,
      gepek: {
        id: null,
        epulet: '',
        emelet: '',
        terem: '',
        gep: ''
      },
      gepeks: []
    }
  },
  methods: {
    async loadData () {
     let Response = await fetch('http://127.0.0.1:8000/api/gepeks')
     let data = await Response.json()
     this.statues = data
    },
    mounted() {
    this.loadData()
  }
  }
}
</script>

<style>
.card{
  width: 18rem;
}

</style>