<template>
  <div>
    <main-header></main-header>
      <!--<main-content>-->

      <!--</main-content>-->


      <nuxt />
      <main-footer></main-footer>
  </div>
</template>
<script>
    import mainHeader from '~/components/header.vue'
    import mainFooter from '~/components/footer.vue'
//    import mainContent from '~/components/content.vue'

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