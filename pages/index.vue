<template>
  <section class="container">
    <div>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias debitis eveniet facere laborum modi molestias ratione sunt? Atque autem dolores dolorum facere fugit ipsam optio placeat quaerat, reiciendis totam veniam.d
    </div>
      <mdb-btn color="red">MDB Button</mdb-btn>
  </section>
</template>

<script>
//import Logo from '~/components/Logo.vue'
import { mdbBtn } from 'mdbvue'

export default {

  components: {
      mdbBtn
  },
    data(){
      return {
          posts:[
              {title:'testing title', description:'testing description'}
          ]
      }
    }
}

</script>