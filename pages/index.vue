<template>
  <section class="container">
    <div>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias debitis eveniet facere laborum modi molestias ratione sunt? Atque autem dolores dolorum facere fugit ipsam optio placeat quaerat, reiciendis totam veniam.d
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
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