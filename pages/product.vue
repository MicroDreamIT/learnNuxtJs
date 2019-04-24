<template>
    <div>
        <div class="container mt-lg-5">
            <div class="row">
                <div class="col-md-6">
                    <no-ssr v-if="images.length>0">
                        <gallery :images="images" :index="index" @close="index = null"></gallery>
                        <div
                                class="image"
                                v-for="(image, imageIndex) in images"
                                :key="imageIndex"
                                @click="index = imageIndex"
                                :style="{ backgroundImage: 'url(' + image + ')', width: '200px', height: '200px' }"
                        ></div>
                    </no-ssr>
                </div>
                <div class="col-md-6">
                    <div>
                        <h5>{{product.name}}</h5>
                    </div>
                    <div v-if="selectedSize.hasOwnProperty('id')">
                        <strong class="text-danger ">{{withoutDiscountPrice}}</strong> <strike>{{withDiscountPrice}}</strike> <strong>{{selectedSize.discount? selectedSize.discount+'% off':''}}</strong>
                    </div>
                    <hr>
                    <div class="form-group">
                        <label>
                            <strong>Size</strong>
                        </label>
                        <select v-model="selectedSize" class="form-control">
                            <option v-for="(size, index) in product.size" :key="size.id" :value="size">{{size.name}}</option>
                        </select>
                    </div>
                    <div>
                        <button @click="addToCart(selectedSize)" class="btn btn-block purple-gradient">add to cart</button>
                    </div>
                </div>
            </div>


        </div>
    </div>
</template>

<script>
    export default {
        name: "product",
        data(){
            return {
                images:[],
                index:null,
                selectedSize:{},
                product:{
                    id:1,
                    name:'Navy Fish Print Half Sleeves T-Shirt And Short Set',
                    images: [
                        'https://dummyimage.com/800/ffffff/000000',
                        'https://dummyimage.com/800/ffffff/000000',
                        'https://dummyimage.com/800/000000/ffffff',
                        'https://dummyimage.com/400/000000/ffffff',
                    ],
                    index: null,
                    size:[
                        {id:1, name:'2-3 years', price:450, default:false, discount: 30},
                        {id:2, name:'3-7 years', price:550, default:true, discount: 40},
                        {id:3, name:'7-10 years', price:650, default:false, discount: 50},
                    ]
                }
            }
        },
        computed:{
            withoutDiscountPrice(){
                return this.selectedSize.price
            },
            withDiscountPrice(){
                let discount = parseFloat(this.selectedSize.discount)
                let price = parseFloat(this.selectedSize.price)

                return price - (price*discount/100)
            },

        },
        created(){
            this.images = this.product.images // suppose to be from axios
            this.selectedSize = this.getDefaultSize(this.product.size)
        },
        head(){
            return {
                title:'hello I am about',
                meta:[
                    {name:'description', content:'my custom description'}
                ]
            }
        },
        methods:{
            getDefaultSize(size){
                return size.filter(val=>val.default)[0]
            },
            addToCart(selected){
                // store in session
                alert('product id ' + this.product.id +' selected size id ' + selected.id)
            }
        }

    }
</script>

<style scoped>
    .image {
        float: left;
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center center;
        border: 1px solid #ebebeb;
        margin: 5px;
    }
</style>