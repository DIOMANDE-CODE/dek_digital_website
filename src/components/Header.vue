<template>
  <div>
    <!-- ======= Header ======= -->
    <header id="header" class="header fixed-top" data-scrollto-offset="0">
      <div
        class="
          container-fluid
          d-flex
          align-items-center
          justify-content-between
        "
      >
        <a
          href="index.html"
          class="logo d-flex align-items-center scrollto me-auto me-lg-0"
        >
          <!-- Uncomment the line below if you also wish to use an image logo -->
          <!-- <img src="../assets/img/logo.png" alt=""> -->
          <h1>
            <span style="color: #f15d22">DEK-DIGITAL </span
            ><span style="color: #0b3146"> + </span><span></span>
          </h1>
        </a>

        <nav id="navbar" class="navbar">
          <ul>
            <li class="dropdown">
              <a href="#"><span>Acceuil</span> </a>
            </li>

            <li>
              <a class="nav-link scrollto" href="index.html#about"
                >Qui sommes-nous ?</a
              >
            </li>
            <li>
              <a class="nav-link scrollto" href="index.html#services"
                >Nos Services</a
              >
            </li>
            <li>
              <a class="nav-link scrollto" href="index.html#contact"
                >Nous joindre</a
              >
            </li>
          </ul>
          <i class="bi bi-list mobile-nav-toggle d-none"></i>
        </nav>
        <!-- .navbar -->
      </div>
    </header>
    <!-- End Header -->

    <!-- Carrousel -->
    <div
      id="carouselExampleSlidesOnly"
      class="carousel slide"
      data-ride="carousel"
    >
      <div class="carousel-inner" >
        <div class="carousel-item active">
          <img
            class="d-block w-100 img-fluid animated"
            src="../assets/img/gif_1.gif"
            alt="First slide"
          />
        </div>
        <div class="carousel-item">
          <img
            class="d-block w-100 img-fluid animated"
            src="../assets/img/consultation.png"
            alt="First slide"
          />
        </div>
        <div class="carousel-item">
          <img
            class="d-block w-100 img-fluid animated"
            src="../assets/img/banner2.jpg"
            alt="First slide"
          />
        </div>
      </div>
    </div>

    <!-- End Carrousel -->
    <section id="hero-animated" class="hero-animated d-flex align-items-center">
      <div
        class="
          container
          d-flex
          flex-column
          justify-content-center
          align-items-center
          text-center
          position-relative
        "
        data-aos="zoom-out"
      >
        <h2>Bienvenue à <span>DEK DIGITAL +</span></h2>
        <p>
          Et voluptate esse accusantium accusamus natus reiciendis quidem
          voluptates similique aut.
        </p>
        <div class="d-flex">
          <a
            href="https://www.youtube.com/watch?v=LXb3EKWsInQ"
            class="glightbox btn-watch-video d-flex align-items-center"
            ><i class="bi bi-play-circle"></i><span>Voir la vidéo</span></a
          >
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  name: "Header",
};
</script>