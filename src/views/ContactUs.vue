<template>
    <div class="contact-us">
        <div class="img">
            <img src="@/assets/images/contact-us.jpg" alt="">
        </div>
        <div class="space"></div>
        <div class="text">
            <h2>Contact Us</h2>
            <span>Let's get in touch</span>
        </div>
        <div class="form">
            <div class="form-data">
                <div class="form-group mb-5">
                    <label for="">Name</label>
                    <input type="text" placeholder="Enter your name" >
                </div>
                <div class="form-group mb-5">
                    <label for="">Email</label>
                    <input type="text" placeholder="Enter your Email">
                </div>
                <div class="form-group mb-5">
                    <label for="">Phone</label>
                    <input type="text" placeholder="Enter your phone">
                </div>
                <div class="form-group mb-5">
                    <label for="">Address</label>
                    <textarea name="" id="" cols="30" rows="3" class="form-control" placeholder="Enter your address"></textarea>
                </div>
                <div class="form-group mb-5">
                    <label for="">Message</label>
                    <textarea name="" id="" cols="30" rows="4" class="form-control" placeholder="Feel free to write us"></textarea>
                </div>
                <button class="btn btn-success">Submit</button>
            </div>
            <div class="map">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d794.96138933151!2d96.13091972674002!3d16.837824966492192!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30c1950017207cd5%3A0xe9fa12534c33c00c!2sLifeline%20Group%20of%20Companies!5e0!3m2!1sen!2smm!4v1688320014597!5m2!1sen!2smm" width="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .contact-us {
        position: relative;
    }

    .contact-us .img {
    }
    .contact-us img {
        width: 100%;
        height: 800px;
        object-fit: cover;
        filter: brightness(.8);
    }

    .text {
        position: absolute;
        top: 20%;
        left: 10%;
    }

    .text h2 {
        color: #fff;
        font-weight: bold;
    }

    .text span {
        color: #fff;
        font-size: 30px;
    }

    .form {
        background: #fff;
        padding: 50px 30px;
        display: flex;
        gap: 20px;
        width: 1300px;
        margin-top: -90px;
        position: absolute;
        top: 70%;
        left: 50%;
        transform: translate(-50%, -50%);
        border-radius: 7px;
    }

    .form-group {
        display: flex;
        flex-direction: column;
    }

    .form-group input {
        border: 1px solid rgb(223, 223, 223);
        padding: 10px 20px;
        border-radius: 7px;
    }

    .form-group input:focus {
        outline: none;
    }

    .form .form-data {
        width: 600px;
    }
    .form .map {
        width: 600px;
        padding: 25px;
    }

    .form .map iframe {
        height: 500px;
    }
   
    .space {
        height: 400px;
        background: #f2f2f2;
    }

    @media (max-width: 1600px) {
        .contact-us {
            position: relative;
        }
        .contact-us img {
            width: 100%;
            height: 600px;
            object-fit: cover;
            filter: brightness(.8);
        }
    
        .text {
            position: absolute;
            top: 10%;
            left: 10%;
        }
    
        .text h2 {
            font-size: 24px;
        }
    
        .text span {
            font-size: 22px;
        }
    
        .form {
            padding: 50px 30px;
            gap: 20px;
            width: 1000px;
            margin-top: -90px;
            position: absolute;
            top: 70%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    
        .form-group {
            display: flex;
            flex-direction: column;
        }
    
        .form-group input {
            padding: 8px 20px;
            border-radius: 7px;
        }
    
        .form-group input:focus {
            outline: none;
        }
    
        .form .form-data {
            width: 600px;
        }
        .form .map {
            width: 600px;
            padding: 25px;
        }
    
        .form .map iframe {
            height: 500px;
        }
       
        .space {
            height: 400px;
            background: #f2f2f2;
        }
    }

</style>
