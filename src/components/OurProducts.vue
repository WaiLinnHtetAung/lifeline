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
                        <span class="badge rounded-pill" v-for="(ing, index) in product.ingredients" :key="index">{{ing}}</span>

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
                    title: "Bherumn-S",
                    src: require("@/assets/images/Principlewise/Bherumn-S.png"),
                    ingredients: ['Cefoperazone 1g', 'Sulbactam 0.5g'],
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "CFM-(Inj)",
                    src: require("@/assets/images/Principlewise/CFM-(Inj).png"),
                    ingredients: ['Cefepime 1g', 'Sterile water for injection 10ml'],
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "Beniclav-625",
                    src: require("@/assets/images/Principlewise/Beniclav-625.png"),
                    ingredients: ['Amoxicillin', 'Potassium clavulanate'],
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "Benixim-200",
                    src: require("@/assets/images/Principlewise/Benixim-200.png"),
                    ingredients: ['cefixime 50mg/ml'],
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "Benixim-100",
                    src: require("@/assets/images/Principlewise/Benixim-100.png"),
                    ingredients: ['cefexime 100 mg'],
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                
                {
                    id: 1, 
                    title: "Pepcare D",
                    src: require("@/assets/images/Principlewise/Pepcare-D.png"),
                    ingredients: ['Pantoprazole 40mg', 'domperidone 10mg'],
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "Pepcare SR",
                    src: require("@/assets/images/Principlewise/Pepcare-SR.png"),
                    ingredients: ['Pantoprazole 40mg', 'Domperidone 30mg'],
                    description: "Ketoconazole topical (for the skin) (Brand Names: Extina, Kuric, Nizoral A-D, Nizoral Topical, Xolegel) is an antifungal medication used to treat fungal infections of the skin such as athlete's foot.",
                },
                {
                    id: 1, 
                    title: "Rosevast",
                    src: require("@/assets/images/Principlewise/Rosevast-10.png"),
                    ingredients: ['Rosuvastatin 10mg'],
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
        width: 100%;
        height: 200px;
        object-fit: contain;
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
