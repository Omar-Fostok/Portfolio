<template>
  <div id="Contact">
    <Navigation id="nav" />
    <v-main id="content">
      <v-row justify="center">
        <v-col cols="12" sm="10" md="8" lg="6">
          <v-card ref="form" id="cardy">
            <v-card-text>
              <v-text-field
                ref="name"
                v-model="name"
                :error-messages="errorMessages"
                label="Your Name"
                placeholder="John Doe"
                required
              ></v-text-field>
              <v-text-field
                ref="address"
                v-model="address"
                label="Your Email"
                placeholder="contact@example.com"
                required
              ></v-text-field>
              <v-text-field
                ref="city"
                v-model="city"
                label="Subject"
                placeholder="subject"
                required
              ></v-text-field>

              <v-autocomplete
                ref="country"
                v-model="country"
                :items="countries"
                label="Country"
                placeholder="Select..."
                required
              ></v-autocomplete>
              <v-textarea placeholder="Write a message.."></v-textarea>
            </v-card-text>
            <v-divider class="mt-12"></v-divider>
            <v-card-actions>
              <v-btn text style="font-weight: bold"> Cancel </v-btn>
              <v-spacer></v-spacer>
              <v-slide-x-reverse-transition>
                <v-tooltip v-if="formHasErrors" left>
                  <template v-slot:activator="{ on, attrs }">
                    <v-btn
                      icon
                      class="my-0"
                      v-bind="attrs"
                      @click="resetForm"
                      v-on="on"
                    >
                      <v-icon>mdi-refresh</v-icon>
                    </v-btn>
                  </template>
                  <span>Refresh form</span>
                </v-tooltip>
              </v-slide-x-reverse-transition>
              <v-btn id="batt" text @click="submit"> Send Message </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <div class="social">
            <a
              href="https://ms-my.facebook.com/omar.fustok/photos"
              target="_blank"
            >
              <i class="fab fa-facebook-square fa-lg" id="f"></i>
            </a>
            <a href=" mailto: omar6817167@gmail.com" target="_blank">
              <i class="fab fa-google fa-lg" id="g"></i>
            </a>
            <a href="https://wa.me/963945281526" target="_blank">
              <i class="fab fa-whatsapp fa-lg" id="w"></i>
            </a>

            <a
              href=" https://www.linkedin.com/in/omar-fostok-b9060a206/"
              target="_blank"
            >
              <i class="fab fa-linkedin fa-lg" id="l"></i>
            </a>
          </div>
        </v-col>
      </v-row>
    </v-main>
    <v-footer id="footer" class="pa-3" color="black" height="37%" dark>
      <v-spacer></v-spacer>
      <div class="caption">
        omar fostok &nbsp; &copy; {{ new Date().getFullYear() }}
      </div>
      <v-spacer></v-spacer>
    </v-footer>
  </div>
</template>
<script>
import Navigation from "../components/Navigation.vue";

export default {
  name: "Contact",
  components: {
    Navigation,
  },
  data: () => ({
    countries: [
      "Afghanistan",
      "Albania",
      "Algeria",
      "Andorra",
      "Angola",
      "Anguilla",
      "Antigua &amp; Barbuda",
      "Argentina",
      "Armenia",
      "Aruba",
      "Australia",
      "Austria",
      "Azerbaijan",
      "Bahamas",
      "Bahrain",
      "Bangladesh",
      "Barbados",
      "Belarus",
      "Belgium",
      "Belize",
      "Benin",
      "Bermuda",
      "Bhutan",
      "Bolivia",
      "Bosnia &amp; Herzegovina",
      "Botswana",
      "Brazil",
      "British Virgin Islands",
      "Brunei",
      "Bulgaria",
      "Burkina Faso",
      "Burundi",
      "Cambodia",
      "Cameroon",
      "Cape Verde",
      "Cayman Islands",
      "Chad",
      "Chile",
      "China",
      "Colombia",
      "Congo",
      "Cook Islands",
      "Costa Rica",
      "Cote D Ivoire",
      "Croatia",
      "Cruise Ship",
      "Cuba",
      "Cyprus",
      "Czech Republic",
      "Denmark",
      "Djibouti",
      "Dominica",
      "Dominican Republic",
      "Ecuador",
      "Egypt",
      "El Salvador",
      "Equatorial Guinea",
      "Estonia",
      "Ethiopia",
      "Falkland Islands",
      "Faroe Islands",
      "Fiji",
      "Finland",
      "France",
      "French Polynesia",
      "French West Indies",
      "Gabon",
      "Gambia",
      "Georgia",
      "Germany",
      "Ghana",
      "Gibraltar",
      "Greece",
      "Greenland",
      "Grenada",
      "Guam",
      "Guatemala",
      "Guernsey",
      "Guinea",
      "Guinea Bissau",
      "Guyana",
      "Haiti",
      "Honduras",
      "Hong Kong",
      "Hungary",
      "Iceland",
      "India",
      "Indonesia",
      "Iran",
      "Iraq",
      "Ireland",
      "Isle of Man",
      "Israel",
      "Italy",
      "Jamaica",
      "Japan",
      "Jersey",
      "Jordan",
      "Kazakhstan",
      "Kenya",
      "Kuwait",
      "Kyrgyz Republic",
      "Laos",
      "Latvia",
      "Lebanon",
      "Lesotho",
      "Liberia",
      "Libya",
      "Liechtenstein",
      "Lithuania",
      "Luxembourg",
      "Macau",
      "Macedonia",
      "Madagascar",
      "Malawi",
      "Malaysia",
      "Maldives",
      "Mali",
      "Malta",
      "Mauritania",
      "Mauritius",
      "Mexico",
      "Moldova",
      "Monaco",
      "Mongolia",
      "Montenegro",
      "Montserrat",
      "Morocco",
      "Mozambique",
      "Namibia",
      "Nepal",
      "Netherlands",
      "Netherlands Antilles",
      "New Caledonia",
      "New Zealand",
      "Nicaragua",
      "Niger",
      "Nigeria",
      "Norway",
      "Oman",
      "Pakistan",
      "Palestine",
      "Panama",
      "Papua New Guinea",
      "Paraguay",
      "Peru",
      "Philippines",
      "Poland",
      "Portugal",
      "Puerto Rico",
      "Qatar",
      "Reunion",
      "Romania",
      "Russia",
      "Rwanda",
      "Saint Pierre &amp; Miquelon",
      "Samoa",
      "San Marino",
      "Satellite",
      "Saudi Arabia",
      "Senegal",
      "Serbia",
      "Seychelles",
      "Sierra Leone",
      "Singapore",
      "Slovakia",
      "Slovenia",
      "South Africa",
      "South Korea",
      "Spain",
      "Sri Lanka",
      "St Kitts &amp; Nevis",
      "St Lucia",
      "St Vincent",
      "St. Lucia",
      "Sudan",
      "Suriname",
      "Swaziland",
      "Sweden",
      "Switzerland",
      "Syria",
      "Taiwan",
      "Tajikistan",
      "Tanzania",
      "Thailand",
      `Timor L'Este`,
      "Togo",
      "Tonga",
      "Trinidad &amp; Tobago",
      "Tunisia",
      "Turkey",
      "Turkmenistan",
      "Turks &amp; Caicos",
      "Uganda",
      "Ukraine",
      "United Arab Emirates",
      "United Kingdom",
      "United States",
      "Uruguay",
      "Uzbekistan",
      "Venezuela",
      "Vietnam",
      "Virgin Islands (US)",
      "Yemen",
      "Zambia",
      "Zimbabwe",
    ],
    errorMessages: "",
    name: null,
    address: null,
    city: null,
    state: null,
    zip: null,
    country: null,
    formHasErrors: false,
  }),

  computed: {
    form() {
      return {
        name: this.name,
        address: this.address,
        city: this.city,
        state: this.state,
        zip: this.zip,
        country: this.country,
      };
    },
  },

  watch: {
    name() {
      this.errorMessages = "";
    },
  },

  methods: {
    addressCheck() {
      this.errorMessages =
        this.address && !this.name ? `Hey! I'm required` : "";

      return true;
    },
    resetForm() {
      this.errorMessages = [];
      this.formHasErrors = false;

      Object.keys(this.form).forEach((f) => {
        this.$refs[f].reset();
      });
    },
    submit() {
      this.formHasErrors = false;

      Object.keys(this.form).forEach((f) => {
        if (!this.form[f]) this.formHasErrors = true;

        this.$refs[f].validate(true);
      });
    },
  },
};
</script>
<style scoped>
.social {
  text-align: center;
}
#f:hover,
#g:hover,
#w:hover,
#l:hover {
  color: #1976d2;
}
#f,
#g,
#w,
#l {
  margin: 20px;
  color: rgb(240, 240, 240);
  transition-property: color;
  transition-duration: 0.25s;
}

#batt {
  color: #1976d2;
  font-weight: bold;
}
#content {
  background-color: rgba(255, 255, 255, 0.05);
}
#Contact {
  background-image: url("../assets/images/550656.jpg");
  background-size: cover;
  position: relative;
}
#footer {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  margin-bottom: -37px;
}

#cardy {
  background-color: rgb(240, 240, 240);
  margin-top: 145px;
  margin-bottom: 152px;
}
#nav {
  position: sticky;
  top: 0;
  z-index: 10;
}
@media only screen and (min-width: 960px) {
  #f,
  #g,
  #w,
  #l {
    font-size: 30px;
  }
}
</style>
