<template>
    <div class="our-products">
        <div class="header-container mb-5">
            <div class="header">
                <div class="title">OUR PRODUCTS</div>
                <div class="all">All Products <i class="fa-solid fa-arrow-up"></i></div>
            </div>
            <div class="underline"></div>
        </div>

        <div class="products">
            <div class="row">
                <div class="col-lg-3 col-md-6 text-center mb-5 all-products"  v-for="(product, index) in products" :key="index">
                    <img :src="product.src" alt="">
                    <div class="product-text text-center mt-3">
                        <span class="badge rounded-pill">ingredient</span>
                        <span class="badge rounded-pill">ingredient</span>
                        <span class="badge rounded-pill">ingredient</span>

                        <h2>{{product.title}}</h2>
                        <p>{{product.description}}</p>
                        <div class="btn-group">
                            <button class="btn btn-outline-primary">All Products</button>
                            <button class="btn btn-outline-primary">Detail</button>
                        </div>
                    </div>
                </div>
                
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        setup() {
            let products = [
                {
                    id: 1, 
                    title: "XTRACAL HD",
                    src: require("@/assets/images/product1.jpg"),
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "CALYZID",
                    src: require("@/assets/images/product2.jpg"),
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "ARTHOCERIN",
                    src: require("@/assets/images/product3.jpg"),
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "AMINOVIT",
                    src: require("@/assets/images/product4.png"),
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "AMINOVIT",
                    src: require("@/assets/images/products/product1.jpg"),
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "AMINOVIT",
                    src: require("@/assets/images/products/product2.jpg"),
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "AMINOVIT",
                    src: require("@/assets/images/products/product3.webp"),
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "AMINOVIT",
                    src: require("@/assets/images/products/product4.png"),
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
            ];

            return {products}
        }
    }
</script>

<style scoped>
    .our-products {
        padding: 80px 15%;
    }

    .products img {
        width: 70%;
        height: 200px;
        object-fit: cover;
    }

    .products .badge {
        background: var(--sec-color);
        margin-right: 2px;
    }

    .products h2{
        margin: 15px auto;
        font-weight: bold;
    }

    .products p {
        font-size: 13px;
        color: #333;
    }

    .all-products {
        margin-bottom: 80px !important;
    }

</style>
