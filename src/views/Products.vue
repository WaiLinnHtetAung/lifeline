<template>
    <div class="banner-img">
        <img src="@/assets/images/products-banner.jpg" alt="">
    </div>
    <div class="products">
        <div class="row">
            <div class="col-lg-3 col-md-4 col-sm-12 pe-0">
                <div class="menu  w-100">
                    <router-link to="/product-service/catalog" :class="{active: slug == 'catalog'}">Products Catalog</router-link>
                    <router-link to="/products/all" :class="{active: slug == 'all'}">All Products</router-link>
                    <router-link :to="'/products/'+category.name" :class="{active: slug == category.name}" v-for="(category, i) in categories" :key="i">{{category.name}}</router-link>
                </div>
            </div>
            <div class="col-lg-9 col-md-8 col-sm-12">
                <div class="header">
                    <div class="slug">{{slug.toUpperCase()}}</div>
                    <div class="search">
                        <input type="text" placeholder="search" class="input">
                        <input type="button" value="Search" class="button">
                    </div>
                </div>
                <div class="content">
                    <div class="row" v-if="filteredProducts.length > 0">
                        <div class="col-lg-4 col-md-6 col-sm-12 mb-3" v-for="(product, i) in filteredProducts" :key="i" >
                            <div class="product-card">
                                <img :src="product.img" alt="">
                                <div class="divider"></div>
                                <div class="ingredient">
                                    <span class="rounded-pill" v-for="(ingre, i) in product.ingredient" :key="i">{{ingre}}</span>
                                </div>
                                <h2>{{product.name}}</h2>
                                <div class="btn">
                                    <button>Detail</button>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div v-else class="no-product">
                        No Products
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import { onMounted, onUpdated, ref, watch } from 'vue'
    import { useStore } from 'vuex';
    import { useRouter } from 'vue-router';
    export default {
        props: ['slug'],

        setup(props) {
            const store = useStore();
            const router = useRouter();
            const categories = ref([]);
            const products = ref([]);
            const filteredProducts = ref([]);
            const currentRoute = ref('');

            router.afterEach(to => {
                currentRoute.value = to.path;
            })

            onMounted(() => {
                window.scrollTo(0,0)
                categories.value = store.getters.getCategories;
                products.value = store.getters.getProducts;
                filteredProducts.value = products.value;
            })

            onUpdated(() => {
                if(props.slug == 'all') {
                    filteredProducts.value = store.getters.getProducts;
                } else {
                    filteredProducts.value = products.value.filter(product => product.category == props.slug);
                }
            })



            return {categories, products, currentRoute, filteredProducts}
        }
    }
</script>

<style scoped>
    .banner-img {
        width: 100%;
        height: 300px;
        padding: 0px 15%;
    }

    .banner-img img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .products {
        padding: 20px 15% 30px;
    }

    .products .menu {
        display: flex;
        flex-direction: column;
        background-color: #e5ecf1;
    }

    .products .menu a {
        text-decoration: none;
        padding: 11px 25px;
        transition: .3s ease;
        color: #000;
    }

    .products .menu a:hover {
        background-color: #3a82a3;
        color: #fff;
    }

    .active {
        background-color: #3a82a3;
        color: #fff !important;
    }

    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 30px;
    }

    .header .slug {
        background: transparent;
        border: 2px solid var(--main-color);
        padding: 10px 50px;
        border-radius: 5px;
        font-size: 10px;
        font-weight: bold;
    }

    .search .input {
        width: 500px;
        background: #ebeaea;
        padding: 10px 20px;
    }

    .search .button {
        background: var(--sec-color);
        color: #fff;
        font-weight: bold;
        padding: 10px 20px;
    }

    .search input:focus {
        outline: none;
    }

    .product-card {
        background-color: #eee;
        border-radius: 5px;
        padding: 0 0 10px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .product-card img {
        width: 100%;
        height: 200px;
        object-fit: contain;
    }

    .product-card .divider {
        width: 100%;
        height: 1px;
        background: var(--main-color);
        margin: -10px 0 15px;
    }

    .ingredient {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 10px;
    }

    .ingredient span {
        background: var(--sec-color);
        color: #fff;
        padding: 0px 15px;
        font-size: 12px;
    }

    .product-card h2 {
        margin: 20px auto;
        font-weight: bold;
        font-size: 24px;
        text-align: center;
    }

    .product-card .btn {
        display: flex;
        justify-content: center;
    }
    .product-card button {
        border: 2px solid var(--main-color);
        padding: 3px 15px;
        border-radius: 5px;
    }

    .no-product {
        text-align: center;
        font-size: 40px;
        font-weight: bold;
        margin-top: 30px;
    }

    @media(max-width: 1600px) {
        .banner-img {
            height: 230px;
            padding: 0px 9%;
        }
    
        .products {
            padding: 20px 9% 30px;
        }
    
    
        .products .menu a {
            padding: 8px 20px;
            font-size: 14px;
        }
    
        .header {
            margin-bottom: 20px;
        }
    
        .header .slug {
            padding: 8px 20px;
            font-size: 10px;
        }
    
        .search .input {
            width: 450px;
            padding: 8px 20px;
        }
    
        .search .button {
            padding: 8px 20px;
        }
        .product-card {
            padding: 0 0 10px;
        }
    
        .product-card img {
            width: 130px;
            height: 150px;
        }
    
        .product-card .divider {
            width: 100%;
            height: 1px;
            margin: -10px 0 15px;
        }
    
        .ingredient span {
            padding: 0px 15px;
            font-size: 11px;
        }
    
        .product-card h2 {
            margin: 10px auto;
            font-size: 18px;
        }
    
        .product-card button {
            padding: 3px 15px;
            border-radius: 5px;
            font-size: 13px;
        }
    
        .no-product {
            font-size: 30px;
        }
    }
</style>
