<template>
  <section class="container">
    <div>
        <div class="alert alert-primary" role="alert">
            A simple primary alert—check it out!
        </div>
    </div>
  </section>
</template>

<script>
//import Logo from '~/components/Logo.vue'

export default {

    components: {

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