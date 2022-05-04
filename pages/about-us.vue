<template>
  <div>
    <section class="we-belive-section">
      <div class="belive-text-container">
        <h1>We believe in everyone's power to do good</h1>
        <v-btn large color="primary">
          <v-icon left color="red">mdi-firefox</v-icon> Add Ecosia to Firefox
        </v-btn>
      </div>
    </section>
    <section class="social-business-section">
      <v-row>
        <v-col cols="col-4" />
        <v-col cols="col-4">
          <p class="main-title">
            Ecosia is a social business founded in 2009 after a trip around the
            world
          </p>
        </v-col>
        <v-col cols="col-4" />
      </v-row>
      <v-row>
        <v-col cols="col-4"></v-col>
        <v-col cols="col-4" class="business-text-container">
          <v-col cols="col-3" v-for="(period, index) in periods" :key="index">
            <p class="title">{{ period.time }}</p>
            <p class="subtitle">{{ period.title }}</p>
            <p class="line"></p>
            <p>{{ period.content }}</p>
          </v-col>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>
    <section class="step-inside-section">
      <v-row>
        <v-col cols="col-4"></v-col>
        <v-col cols="col-4" class="step-inside-container">
          <p class="main-title">Step inside!</p>
          <p class="main-subtitle">
            Meet the humans who make Ecosia and learn what it's like to work
            here
          </p>
          <v-btn v-if="!play" fab large dark @click="play = true">
            <v-icon color="red">mdi-youtube</v-icon>
          </v-btn>
          <video v-else controls autoPlay="true" class="video-wrapper">
            <source
              src="https://d3fme2ivr1xlgj.cloudfront.net/240719_Ecosia_hiringvideo_subbed_titled.mp4"
              type="video/mp4"
            />
          </video>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>
    <section class="hiring-section">
      <v-row>
        <v-col cols="col-4"></v-col>
        <v-col cols="col-4" class="hire-container">
          <p class="main-title">We're hiring!</p>
          <p class="main-subtitle">
            Want to help change the world? Let's team up. Apply to help us build
            great products and services that can make the world a more
            sustainable place. We can't wait to hear from you.
          </p>
          <v-btn large color="primary">
            <v-icon left color="red">mdi-human-capacity-increase</v-icon>
            Open positions
          </v-btn>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>
    <section class="contact-us-section">
      <v-row>
        <v-col cols="col-4"></v-col>
        <v-col cols="col-4" class="contact-container">
          <p class="main-title">Contact us</p>
          <p class="main-subtitle">
            For questions about Ecosia check our FAQ first. If you don't see
            what you are looking for, drop us a line!
          </p>
          <v-container fluid>
            <v-form ref="form" v-model="valid" lazy-validation>
              <v-textarea
                v-model="message"
                :rules="messageRules"
                label="Message"
                required
                outlined
                shaped
              ></v-textarea>

              <v-text-field
                v-model="email"
                :rules="emailRules"
                label="E-mail"
                required
                outlined
              ></v-text-field>

              <v-select
                v-model="select"
                :items="items"
                :rules="[(v) => !!v || 'Item is required']"
                label="Item"
                required
                outlined
              ></v-select>

              <v-btn
                :disabled="!valid"
                color="success"
                class="mr-4"
                @click="validate"
              >
                Send
              </v-btn>
            </v-form>
          </v-container>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>
  </div>
</template>

<script>
export default {
  name: 'AboutUsPage',
  data() {
    return {
      periods: this.getTimePeriods(),
      play: false,
      valid: true,
      message: '',
      messageRules: [(v) => !!v || 'Message is required'],
      email: '',
      emailRules: [
        (v) => !!v || 'E-mail is required',
        (v) => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      select: null,
      items: [
        'Tech support',
        'General enquiry',
        'Press enquiry',
        'Tree-planting partnership',
      ],
      checkbox: false,
    }
  },
  methods: {
    validate() {
      this.$refs.form.validate()
    },
    reset() {
      this.$refs.form.reset()
    },
    resetValidation() {
      this.$refs.form.resetValidation()
    },
    getTimePeriods() {
      return [
        {
          time: 'December 2009',
          title: 'Ecosia is born',
          content:
            'Christian founded Ecosia.org after a trip around the world helped him understand the problems of deforestation.',
        },
        {
          time: '2009 - 2011',
          title: "People's choice",
          content:
            'Ecosia won several awards for its clever concept and speedy growth in Europe and beyond.',
        },
        {
          time: 'April 2014',
          title: 'First German B Corp',
          content:
            'Ecosia was the first German company to become a B Corporation thanks to its social business model.',
        },
        {
          time: 'April 2018',
          title: '25 million trees',
          content:
            'A planting milestone! That same year, Ecosia also builds its own solar energy plant to power every search.',
        },
      ]
    },
  },
}
</script>

<style lang="scss" scoped>
$alice-blue: aliceblue;

.main-title {
  font-size: 2.5em;
  text-align: center;
}

.main-subtitle {
  font-size: 1.5em;
  text-align: center;
}

.we-belive-section {
  background-color: $alice-blue;

  .belive-text-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 50vh;

    h1 {
      font-size: 3em;
      padding: 20px 0px;
    }
  }
}

.social-business-section {
  .business-text-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    height: 20vh;

    text-align: center;

    .title {
      text-transform: uppercase;
      color: grey;
    }

    .line {
      border: 3px solid teal;
    }
  }
}

.step-inside-section {
  background-color: $alice-blue;

  .step-inside-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 40vh;

    .video-wrapper {
      max-height: 70%;
    }
  }
}

.hiring-section {
  .hire-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 30vh;
  }
}

.contact-us-section {
  background-color: $alice-blue;
  border: 1px solid red;

  .contact-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 50vh;

    text-align: center;
  }
}
</style>
