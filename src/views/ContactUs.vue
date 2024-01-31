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
        <button class="btn">Submit</button>
      </div>
      <div class="address">
        <h3>Meet Us</h3>
        <div class="address-card">
          <div class="address-icon">
            <i class="fa-solid fa-location-dot mt-5"></i>
          </div>

          <p class="location">
            No.13, HlaingMyintHmo 7 th St, Hlaing Township, Yangon
          </p>
        </div>
        <div class="address-card">
          <div class="address-icon">
            <i class="fa-solid fa-square-phone"></i>
          </div>
          <p>
            +959 - 2343423442<br />
            +959 - 4432325902
          </p>

          <p></p>
        </div>
        <div class="address-card">
          <div class="address-icon">
            <i class="fa-solid fa-envelope"></i>
          </div>
          <p class="text-center">inquiry@lifelinemyanmar.com</p>
          <p>&nbsp;</p>
        </div>
        <div class="map"></div>
      </div>
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
  width: 420px;
  padding: 0px 50px;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
}

.form-group input {
  border: 1px solid rgb(223, 223, 223);
  padding: 10px 20px;
  border-radius: 7px;
  gap: 10px;
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

.btn {
  display: flex;
  width: 100px;
  padding: 10px;
  margin-left: 50px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 10px;
  background: #01ffff;
  color: #fff;
}

.space {
  height: 400px;
  background: #f2f2f2;
}

.address {
  display: flex;
  width: 650px;
  align-items: flex-start;
  align-content: flex-start;
  flex-wrap: wrap;
}

.address-card {
  display: flex;
  text-align: center;
  align-items: center;
  gap: 10px;
}
.address-card p {
  margin-top: 15px;
  font-size: 14px;
}
.address-card .location {
  margin-top: 35px;
}

.address-card i {
  font-size: 35px;
  color: var(--sec-color);
}

.address-card h3 {
  font-weight: bold;
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
    padding: 0px 9%;
    gap: 10px;
  }

  .address-card h3 {
    font-size: 24px;
  }
}

@media (max-width: 1400px) {
  .address {
    padding: 0px 6%;
    gap: 20px;
  }
}

@media (max-width: 1200px) {
  .form {
    width: 990px;
  }
  .address {
    display: flex;
    width: 600px;
    align-items: flex-start;
    align-content: flex-start;
    flex-wrap: wrap;
  }
}

@media (max-width: 1080px) {
  .form {
    width: 800px;
  }

  .address {
    display: flex;
    width: 350px;
    align-items: flex-start;
    align-content: flex-start;
    flex-wrap: wrap;
  }

  .address-card {
    text-align: left;
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
