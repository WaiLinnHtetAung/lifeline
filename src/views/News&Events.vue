<template>
    <div class="news-events">
        <div class="row">
            <div class="col-lg-2 col-md-4 col-sm-12 p-0 ">
                <div class="menu  w-100">
                    <router-link to="/news-events/csr-activities" :class="{active: slug == 'csr-activities'}">CSR Activities</router-link>
                    <router-link to="/news-events/news" :class="{active: slug == 'news'}">News</router-link>
                </div>
            </div>
            <div class="col-lg-10 col-md-8 col-sm-12">
                <div class="content">
                    <div v-if="slug == 'csr-activities'"><CsrActivity></CsrActivity></div>
                    <div v-if="slug == 'news'"><News></News></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import News from '../components/news&events/News'
import CsrActivity from '../components/news&events/CsrActivity'
export default {
  components: {
    News, CsrActivity },
        props: ['slug'],
    }
</script>

<style scoped>
.news-events {
    padding: 30px 15%;
}

.news-events .menu {
    display: flex;
    flex-direction: column;
    background-color: #e5ecf1;
}

.news-events .menu a {
    text-decoration: none;
    padding: 11px 25px;
    transition: .3s ease;
    color: #000;
}

.news-events .menu a:hover {
    background-color: #3a82a3;
    color: #fff;
}

.active {
    background-color: #3a82a3;
    color: #fff !important;
}

@media (max-width: 1600px) {
    .news-events {
        padding: 30px 9%;
    }

    .news-events .menu a {
        padding: 9px 25px;
        font-size: 14px;
    }
}

@media (max-width: 1200px) {
    .news-events {
        padding: 30px 3%;
    }

    .news-events .menu a {
        padding: 9px 25px;
        font-size: 14px;
    }
}
</style>
