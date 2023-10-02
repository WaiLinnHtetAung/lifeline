<template>
    <div class="partnership" :class="{hospital: slug == 'hospitals'}">
        <div class="row">
            <div class="col-lg-3 col-md-4 col-sm-12 p-0 ">
                <div class="menu  w-100">
                    <router-link to="/partnership/principles" :class="{active: slug == 'principles'}">Principles</router-link>
                    <router-link to="/partnership/hospitals" :class="{active: slug == 'hospitals'}">Hospitals</router-link>
                </div>
            </div>
            <div class="col-lg-9 col-md-8 col-sm-12">
                <div class="content">
                    <div v-if="slug == 'principles'"><Principle></Principle></div>
                    <div v-if="slug == 'hospitals'"><Hospitals></Hospitals></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Hospitals from '../components/partnership/Hospitals'
import Principle from '../components/partnership/Principle'
export default {
    props: ['slug'],
  components: {
    Hospitals, Principle },
        
    }
</script>

<style scoped>
.partnership {
    padding: 30px 15%;
}

.partnership.hospital {
    background: #efefef;
}

.partnership .menu {
    display: flex;
    flex-direction: column;
    background-color: #e5ecf1;
}

.partnership .menu a {
    text-decoration: none;
    padding: 11px 25px;
    transition: .3s ease;
    color: #000;
}

.partnership .menu a:hover {
    background-color: #3a82a3;
    color: #fff;
}

.active {
    background-color: #3a82a3;
    color: #fff !important;
}

@media (max-width: 1600px) {
    .partnership {
        padding: 30px 9%;
    }

    .partnership .menu a {
        padding: 9px 25px;
        font-size: 14px;
    }
}

@media (max-width: 1200px) {
    .partnership {
        padding: 30px 3%;
    }

    .partnership .menu a {
        padding: 9px 25px;
        font-size: 14px;
    }
}
</style>
