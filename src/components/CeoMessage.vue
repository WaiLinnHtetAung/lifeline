<template>
    <div class="ceo-message">
        <div class="row ">
            <div class="col-lg-4 col-md-4">
                <div class="ceo">
                    <img src="@/assets/images/ceo-photo.jpg" alt="">
                </div>
            </div>
            <div class="col-lg-8 col-md-8 message">
                <div >
                    <h2>CEO Message</h2>
                    <p>This website is intended exclusively for Medicare providers and health care industry professionals to find the latest Medicare news and information affecting ..This website is intended exclusively for Medicare providers and health care industry professionals to find the latest Medicare news and information affecting ..</p>
                    <router-link to="#" class="btn ">Read More</router-link>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .ceo-message {
        padding: 10px 15%;
        background-image: linear-gradient(to right, rgb(86,192,226, .8), rgba(255, 187, 0, 0.5));
        height: 300px;
        margin: 40px auto 80px;
    }

    .ceo-message .ceo {
       margin-top: -33px;
    }
    .ceo-message img {
        width: 350px;
        height: 350px;
        border-radius: 100%;
        object-fit: cover;
        object-position: center;
    }

    .ceo-message .message {
        display: flex;
        justify-content: center;
        align-items: center;
        padding-bottom: 20px;
    }

    .ceo-message .message h2 {
        color: #fff;
        font-weight: bold;
        margin-bottom: 20px;
    }

    .ceo-message .message p {
        color: #333;
    }

    .ceo-message .message .btn {
        background: var(--main-color);
    }
</style>
