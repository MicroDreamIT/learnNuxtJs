<template>
  <div>
    <main-header class="own-mb"></main-header>
      <!--<content>-->
          <!---->
      <!--</content>-->
      <nuxt />

      <main-footer class="mt-lg-5"></main-footer>
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
<style scoped>
    .own-mb{
        margin-bottom: 100px!important;
    }
</style>