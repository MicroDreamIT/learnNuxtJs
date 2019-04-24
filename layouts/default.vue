<template>
  <div>
    <main-header></main-header>
      <!--<content>-->
          <!---->
      <!--</content>-->
      <nuxt />

      <main-footer></main-footer>
  </div>
</template>
<script>
    import mainHeader from '~/components/header.vue'
    import mainFooter from '~/components/footer.vue'


    export default {

        components: {
            mainHeader,mainFooter
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