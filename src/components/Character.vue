<template>
<div class="col-xs-4">
  <div class="thumbnail">
    <h3>{{ character.createdAt }}</h3>
    <img class="img img-responsive" :src="character.url" style="height:250px"/>
    <div class="caption">
      <div class="text-right">
        <button class="btn btn-primary" @click="switchCharacter">
          <span class="glyphicon glyphicon-transfer"></span>
          換一個
        </button>
      </div>
    </div> 
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      character:{}
    }
  },
  methods:{
    fetchCharacter()
    {
      fetch(`http://gank.io/api/random/data/福利/1`,{
        method:'GET'
      }).then(response=>response.json())
        .then(json=>this.character=json.results[0])
        .then(json=>console.log(json))
    },
    switchCharacter()
    {
      this.fetchCharacter();
    }
  },
  created(){
    this.fetchCharacter()
  }
}

</script>

