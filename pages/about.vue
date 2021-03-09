<template>
  <div class="about z-10">
    <div class="about-content">
      <h1 class="about-content-title text-center pb-4">
        About Me
      </h1>
      <b-container fluid class="px-5">
        <b-row class="row d-flex align-items-center">
          <b-col class="col-md-6">
            <img src="../assets/img/tim-mossholder-hrm0hf8pCdU-unsplash.jpg" alt="studio" class="about-image mx-auto d-block">
          </b-col>
          <b-col class="col-md-6">
            <p class="text-center ml-1">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio, ea!
            </p>
          </b-col>
        </b-row>
        <b-row class="row py-4 d-flex align-items-center">
          <b-col class="col-md-6">
            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sapiente molestias laudantium earum dignissimos laboriosam molestiae accusantium aut, labore aliquid corporis, esse repellendus. Tenetur maiores, at sunt dolores, hic repudiandae dicta, veniam nisi possimus blanditiis reprehenderit debitis.
            </p>
          </b-col>
          <b-col>
            <img src="../assets/img/pierre-bamin-_HymxEhaKjQ-unsplash.jpeg" alt="studio" class="about-image mx-auto d-block">
          </b-col>
        </b-row>
        <div class="credits">
          <span>Photos by <a href="https://unsplash.com/@timmossholder?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Tim Mossholder</a> and  <a href="https://unsplash.com/@pierre_bamin?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Pierre Banin</a> on <a href="https://unsplash.com/s/photos/artist?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>
        </div>
      </b-container>
    </div>
  </div>
</template>

<style scoped>
.about {
  background: rgb(109,122,203);
  background: linear-gradient(184deg, rgba(109,122,203,1) 0%, rgba(1,5,17,1) 73%);
  margin-top: -85px;
  color: white;
}

.about-content {
  padding-top: 100px;
  font-family: 'Poppins', sans-serif;
  height: 100%;
}

.about-content-title {
  font-family: 'Abril Fatface', cursive;
}

.about-image {
  height: 250px;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  border-radius: 10px;
  opacity: 75%;
}

.credits {
  font-size: 8px;
}
</style>
