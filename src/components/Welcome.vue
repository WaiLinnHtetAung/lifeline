<template>
  <div class="welcome">
    <h2>Welcome To Lifeline Group of Companies</h2>
    <p>
      Lorem update ispsum dolor sit amet, consectetur adipisicing elit. Tenetur
      maxime esse sunt excepturi odio soluta asperiores vel fuga! Assumenda,
      eius! Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum,
      incidunt at dignissimos sed ipsam nisi Lorem ipsum dolor sit amet
      consectetur adipisicidng elit. Eaque repedfllendus illum molestias dolore
      quae ea atque optio doslorum facere? Sapiente, explicabo. Necessitatibus,
      repellendus totam cum harum magni quia vero odit. quaerat quis asperiores
      magni reprehenderit!
    </p>
    <p>
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quas id modi
      Lorem, ipsum dolor sit amet consectetsur adipisicing elit. Laborum quia
      reprehenderit beatae sit omnis similique sequi nulla veritatis quaerat
      eius. alias exercitationem? Officia consequatur quam perferendis nam,
      animi sapiente!
    </p>
    <br />
    <router-link to="#">Read More</router-link>
  </div>
  <div class="bar">
    <v-progress-linear
      model-value="100"
      height="5"
      striped
      color="#FF8C00"
    ></v-progress-linear>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.welcome {
  padding: 60px 15% 20px;
}

.welcome h2 {
  font-size: 32px;
  font-weight: bolder;
  margin-bottom: 15px;
  color: var(--main-color);
}

.welcome p {
  font-size: 18px;
  text-align: justify;
  text-indent: 50px;
}

.welcome a {
  text-decoration: none;
  background: var(--sec-color);
  color: #fff;
  padding: 10px 15px;
  border-radius: 5px;
}

.bar {
  padding: 0px 15%;
}

@media (max-width: 1600px) {
  .welcome {
    padding: 60px 9% 20px;
  }

  .welcome h2 {
    font-size: 25px;
    font-weight: bolder;
    margin-bottom: 15px;
    color: var(--main-color);
  }

  .welcome p {
    font-size: 15px;
  }

  .welcome a {
    padding: 5px 15px;
    font-size: 12px;
  }

  .bar {
    padding: 0px 9%;
  }
}

@media (max-width: 1200px) {
  .welcome {
    padding: 60px 3% 20px;
  }
}
</style>
