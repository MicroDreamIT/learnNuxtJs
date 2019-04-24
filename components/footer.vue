<template>
    <div>
        <div class="footer-part">
            <div class="container">

                <div class="footer-content">
                    <img src="https://static.hopscotch.in/web2/images/hs-logo.png"/>
                    <ul>
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                    </ul>
                    <span>
                        &copy; 2011-2018 Hopscotch. All rights reserved.
                    </span>
                </div>

            </div>
        </div>
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

<style >
    .footer-part{
        max-height: 50px;
        width: 100%;
        border-top: 1px solid #e6e6e6;
    }
    .footer-part img{
        height: 40px;
        width: auto;
    }
    .footer-content ul{
        display: flex;
        padding-top: 16px;
    }
    .footer-content ul li a{
        padding-right:20px;
        color: #a4a4a4!important;


    }
    .footer-content{
        display: flex;
        color: #a4a4a4;

    }
    .footer-content span{
        padding-top: 16px;
    }
</style>