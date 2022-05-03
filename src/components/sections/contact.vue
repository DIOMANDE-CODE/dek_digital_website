<template>
  <div>
    <!-- ======= Contact Section ======= -->
    <section id="contact" class="contact">
      <div class="container">
        <div class="section-header">
          <h2>Nous joindre</h2>
          <!-- <p>
            Nous sommes disponible pour toutes vos préocupations
          </p> -->
        </div>
      </div>
      <!-- End Google Maps -->

      <div class="container">
        <div class="row gy-5 gx-lg-5">
          <div class="col-lg-4">
            <div class="info">
              <h3>Nos coordonnées</h3>
              <p>
              
              </p>

              <div class="info-item d-flex">
                <i class="bi bi-geo-alt flex-shrink-0"></i>
                <div>
                  <h4>Localisation:</h4>
                  <p>Cocody Rivéra 2</p>
                </div>
              </div>
              <!-- End Info Item -->

              <div class="info-item d-flex">
                <i class="bi bi-envelope flex-shrink-0"></i>
                <div>
                  <h4>Email:</h4>
                  <p>dekdigitalplus@gmail.com</p>
                </div>
              </div>
              <!-- End Info Item -->

              <div class="info-item d-flex">
                <i class="bi bi-phone flex-shrink-0"></i>
                <div>
                  <h4>Appelez-nous :</h4>
                  <p>+225 0759676026</p>
                  <p>+225 0595031694</p>
                  <p>+225 0701101175</p>
                </div>
              </div>
              <!-- End Info Item -->
            </div>
          </div>

          <div class="col-lg-8">
            <form
              class="php-email-form"
              method="POST"
              @submit.prevent="envoyer"
            >
              <div class="row">
                <div class="col-md-6 form-group">
                  <input
                    type="text"
                    name="name"
                    class="form-control"
                    id="name"
                    placeholder="Votre nom"
                    v-model="nom"
                    required
                  />
                </div>
                <div class="col-md-6 form-group mt-3 mt-md-0">
                  <input
                    type="email"
                    class="form-control"
                    name="email"
                    id="email"
                    placeholder="Votre email"
                    v-model="mail"
                    required
                  />
                </div>
              </div>
              <div class="form-group mt-3">
                <input
                  type="text"
                  class="form-control"
                  name="subject"
                  id="subject"
                  placeholder="Sujet"
                  v-model="sujet"
                  required
                />
              </div>
              <div class="form-group mt-3">
                <textarea
                  class="form-control"
                  name="message"
                  placeholder="Message"
                  v-model="message"
                  required
                ></textarea>
              </div>
              <div class="my-3">
                <div class="loading">Loading</div>
                <div class="error-message"></div>
                <div class="alert alert-success" role="alert" v-if="success">
                  {{ success }}
                </div>
              </div>
              <div class="text-center">
                <button type="submit" @submit.prevent="envoyer">
                  Envoyer
                </button>
              </div>
            </form>
          </div>
          <!-- End Contact Form -->
        </div>
      </div>
    </section>
    <!-- End Contact Section -->
  </div>
</template>
<script>

import axios from 'axios'
export default {
  name: "Contact",
  data() {
    return {
      nom: "",
      mail: "",
      sujet: "",
      message: "",
      success: "",
    };
  },
  methods: {
    envoyer() {
      var contact = {
        nom : this.nom,
        mail : this.mail,
        sujet : this.sujet,
        message : this.message
      }
      axios.post('http://127.0.0.1:8000/api/email/', contact)
      .then(
        (response) => {
          this.success = "Votre message a été envoyé";
          this.nom = "",
          this.mail = "",
          this.sujet = "",
          this.message = ""
        }
      )
      .catch((err) => {
        console.log(err);
      })
    },
  },
};
</script>