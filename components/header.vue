<template>
    <div>

        <div class="header-top">
            <div class="container">
                <span>Account</span>
                <span>24x7 Customer care</span>
            </div>

        </div>
        <header>

            <nuxt-link to="/" class="nav-link">Home</nuxt-link>

            <nav class="navbar fixed-top navbar-expand-lg navbar-dark pink scrolling-navbar">
                <div class="container">
                    <div class="navbar-brand-logo pr-4"> </div>

                <nuxt-link class="navbar-brand" to="/"><strong></strong></nuxt-link>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
                        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav mr-auto ">
                        <li class="nav-item pr-4">
                            <nuxt-link class="nav-link" to="/">Discover <span class="sr-only">(current)</span></nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link class="nav-link" to="/product">Moments</nuxt-link>
                        </li>
                    </ul>

                </div>
                </div>
            </nav>


        </header>

    </div>
</template>

<script>
    export default{
        data(){
            return{
            
            
            }
        
        }
    }
</script>
<style scoped>
    .navbar{
        background:#ed54a4!important;
        -webkit-box-shadow: 0 4px 5px 0 rgba(0,0,0,.16), 0 2px 2px 0 rgba(0,0,0,.12);
    }
    .fixed-top{
        top:23px!important;
    }
    .header-top{
        padding: 4px;
        font-size: 13px;
        font-weight: 400;
        background:#ed54a4!important;
        color: white;
        text-align: right;
    }
    .header-top span:nth-child(1){
        padding-right: 15px;
    }
    .navbar-brand-logo{
        position: absolute;
        top: -11px;
        width: 100px;
        left: -85px;
        height: 45px;
        background: url(../static/hopscotch_typeface.svg) no-repeat,url(../static/hop.svg) no-repeat;
    }
    .navbar-nav li a{
        font-weight: 500;
        font-size: 15px;
    }
    .container{    position: relative;}
</style>