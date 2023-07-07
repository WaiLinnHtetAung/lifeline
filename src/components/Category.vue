<template>
    <div class="category">
        <div class="header-container">
            <div class="header">
                <div class="title">CATEGORIES</div>
                <div class="all">All Categories <i class="fa-solid fa-arrow-up"></i></div>
            </div>
            <div class="underline">

            </div>
        </div>

        <div class="categories ">
            <div class="category-item pointer" v-for="(cat, index) in categories" :key="index">
                <img :src="cat.src" alt="">
                <div>{{cat.title}}</div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        setup() {
            let categories = [
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat1.jpg'),
                    title: "Topical Cream"
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat2.jpg'),
                    title: "Anti Allergic"
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat3.jpg'),
                    title: "Neuropathic Panin Reliver"
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat4.jpg'),
                    title: "Anti Platelet"
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat5.jpg'),
                    title: "Antiangina"
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat6.jpg'),
                    title: "Antianxiety Drug"
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat7.webp'),
                    title: "Antibiotic"
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat8.jpg'),
                    title: "Antifibrinolytic"
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat9.webp'),
                    title: "Antihypertensive "
                },
                {
                    id: 1, 
                    src: require('@/assets/images/category/cat10.jpg'),
                    title: "Antipsychotic "
                },
            ];

            return {categories}
        }
    }
</script>

<style scoped>
    .category {
        padding: 80px 15%;
    }

    .categories {
        margin: 50px auto;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 100px;
    }

    .categories .category-item {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 20px;
    }

    .categories .category-item img {
        width: 150px;
        height: 150px;
        border-radius: 100%;
        object-fit: inherit;
    }

    .categories .category-item div {
        font-size: 18px;
        font-weight: bold;
    }
    
</style>
