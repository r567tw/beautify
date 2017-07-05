<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <p>
      <button onclick="javascript:window.location.reload()" class="btn btn-xs btn-warning">
        <span class="glyphicon glyphicon-refresh"></span>
        再換一批
      </button>
    </p>
    <div class="col-xs-12">
        <Character/>
        <Character/>
        <Character/>
      </div>
    </div>
  </div>
</template>

<script>
import Character from './components/Character.vue'

export default {
  name: 'app',
  data () {
    return {
      title: '正妹牆',
      ids:[1,2,3]
    }
  },
  methods:{

  },
  components:{
    Character
  }
}

</script>

