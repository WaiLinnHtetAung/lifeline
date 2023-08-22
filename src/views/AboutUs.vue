<template>
    <div class="about-us">
        <div class="row">
            <div class="col-lg-3 col-md-4 col-sm-12 p-0 ">
                <div class="menu  w-100">
                    <router-link to="/about-us/introduction" :class="{active: slug == 'introduction'}">Introduction</router-link>
                    <router-link to="/about-us/ceo-message" :class="{active: slug == 'ceo-message'}">CEO Message</router-link>
                    <router-link to="/about-us/vision-mission" :class="{active: slug == 'vision-mission'}">Vision & Mission</router-link>
                    <router-link to="/about-us/company-milestone" :class="{active: slug == 'company-milestone'}">Company Milestones</router-link>
                    <router-link to="#">Distribution Network</router-link>
                    <router-link to="#">Regulatory Strength</router-link>
                </div>
            </div>
            <div class="col-lg-9 col-md-8 col-sm-12">
                <div class="content">
                    <div v-if="slug == 'introduction'"><Introduction></Introduction></div>
                    <div v-if="slug == 'ceo-message'"><CeoMessage></CeoMessage></div>
                    <div v-if="slug == 'vision-mission'"><VisionMission></VisionMission></div>
                    <div v-if="slug == 'company-milestone'"><CompanyMilestone></CompanyMilestone></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import CompanyMilestone from '../components/about-us/CompanyMilestone'
import VisionMission from '../components/about-us/VisionMission'
import CeoMessage from '../components/about-us/CeoMessage'
import { onMounted } from 'vue'
    import Introduction from '../components/about-us/Introduction'
export default {
  components: {
    CompanyMilestone,
    VisionMission,
    CeoMessage, Introduction },
        props: ['slug'],
        setup() {
            onMounted(() => {
                window.scrollTo(0,0)
            })
        }
    }
</script>

<style scoped>
    .about-us {
        padding: 30px 15%;
    }

    .about-us .menu {
        display: flex;
        flex-direction: column;
        background-color: #e5ecf1;
    }

    .about-us .menu a {
        text-decoration: none;
        padding: 11px 25px;
        transition: .3s ease;
        color: #000;
    }

    .about-us .menu a:hover {
        background-color: #3a82a3;
        color: #fff;
    }

    .active {
        background-color: #3a82a3;
        color: #fff !important;
    }

    @media (max-width: 1600px) {
        .about-us {
            padding: 30px 9%;
        }

        .about-us .menu a {
            padding: 9px 25px;
            font-size: 14px;
        }
    }

    @media (max-width: 1200px) {
        .about-us {
            padding: 30px 3%;
        }

        .about-us .menu a {
            padding: 9px 25px;
            font-size: 14px;
        }
    }
</style>
