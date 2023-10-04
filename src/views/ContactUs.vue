<template>
  <div class="contact-us">
    <div class="img">
      <img src="@/assets/images/contact-us.jpg" alt="" />
    </div>
    <div class="space"></div>
    <div class="text">
      <h2>Contact Us</h2>
      <span>Let's get in touch</span>
    </div>
    <div class="form shadow">
      <div class="form-data">
        <div class="form-group mb-5">
          <label for="">Name</label>
          <input type="text" placeholder="Enter your name" />
        </div>
        <div class="form-group mb-5">
          <label for="">Email</label>
          <input type="text" placeholder="Enter your Email" />
        </div>
        <div class="form-group mb-5">
          <label for="">Phone</label>
          <input type="text" placeholder="Enter your phone" />
        </div>
        <div class="form-group mb-5">
          <label for="">Address</label>
          <textarea
            name=""
            id=""
            cols="30"
            rows="3"
            class="form-control"
            placeholder="Enter your address"
          ></textarea>
        </div>
        <div class="form-group mb-5">
          <label for="">Message</label>
          <textarea
            name=""
            id=""
            cols="30"
            rows="4"
            class="form-control"
            placeholder="Feel free to write us"
          ></textarea>
        </div>
        <button class="btn btn-success w-100">Submit</button>
      </div>
      <div class="map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d794.96138933151!2d96.13091972674002!3d16.837824966492192!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30c1950017207cd5%3A0xe9fa12534c33c00c!2sLifeline%20Group%20of%20Companies!5e0!3m2!1sen!2smm!4v1688320014597!5m2!1sen!2smm"
          width="100%"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </div>
    </div>
  </div>

  <div class="address">
    <div class="address-card shadow">
      <div class="address-icon">
        <i class="fa-solid fa-location-dot mt-5"></i>
      </div>
      <h3>Lifeline</h3>
      <p class="text-center">
        No.13, HlaingMyintHmo 7 th St, Hlaing Township, Yangon
      </p>
    </div>

    <div class="address-card shadow">
      <div class="address-icon">
        <i class="fa-solid fa-square-phone"></i>
      </div>
      <p class="text-center">+959 - 2343423442</p>
      <p class="text-center">+959 - 4432325902</p>
    </div>

    <div class="address-card shadow">
      <div class="address-icon">
        <i class="fa-solid fa-envelope"></i>
      </div>
      <p class="text-center">inquiry@lifelinemyanmar.com</p>
      <p>&nbsp;</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.contact-us {
  position: relative;
  overflow: hidden;
}

.contact-us img {
  width: 100%;
  height: 800px;
  object-fit: cover;
  filter: brightness(0.8);
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

.address {
  padding: 30px 15.5%;
  background: #f2f2f2;
  display: flex;
  justify-content: center;
  gap: 30px;
  padding-bottom: 90px;
}
.address-card {
  background: #fff;
  width: 25%;
  padding: 20px 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
}

.address-card .address-icon {
  height: 80px;
}

.address-card i {
  font-size: 35px;
  color: var(--sec-color);
  margin: 10px auto 20px;
}

.address-card h3 {
  font-weight: bold;
}

.address-card p {
  margin-bottom: 10px;
}

@media (max-width: 1600px) {
  .contact-us {
    position: relative;
  }
  .contact-us img {
    width: 100%;
    height: 600px;
    object-fit: cover;
    filter: brightness(0.8);
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
    width: 1100px;
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

  .address {
    padding: 30px 9%;
    gap: 30px;
  }

  .address-card h3 {
    font-size: 24px;
  }
}

@media (max-width: 1400px) {
  .address {
    padding: 30px 6%;
    gap: 30px;
  }
}

@media (max-width: 1200px) {
  .form {
    width: 990px;
  }
  .address {
    padding: 30px 0%;
    gap: 60px;
  }
}

@media (max-width: 1080px) {
  .form {
    width: 800px;
  }

  .address {
    gap: 20px;
  }

  .address-card {
    width: 28%;
    padding: 20px 40px;
  }

  .address-card i {
    font-size: 30px;
  }
}

@media (max-width: 830px) {
  .form {
    width: 600px;
  }

  .form .map {
    display: none;
  }

  .address {
    gap: 20px;
    flex-wrap: wrap;
  }

  .address-card {
    width: 30%;
    padding: 20px;
  }

  .address-card h3 {
    font-size: 19px;
  }

  .address-card p {
    font-size: 13px;
  }
}

@media (max-width: 650px) {
  .form {
    width: 500px;
  }

  .address {
    gap: 10px;
  }

  .address-card {
    width: 45%;
    padding: 10px 20px;
  }

  .address-card .address-icon {
    height: 65px;
  }

  .address-card h3 {
    font-size: 19px;
  }

  .address-card p {
    font-size: 14px;
  }
}

@media (max-width: 530px) {
  .form {
    width: 100%;
  }
}

@media (max-width: 420px) {
  .address-card {
    width: 90%;
    padding: 10px 20px;
  }
}
</style>
