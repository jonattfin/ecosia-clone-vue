<template>
  <div>
    <section class="search-engine-section">
      <v-row>
        <v-col cols="col-4"></v-col>
        <v-col cols="col-4" class="search-engine-container">
          <img src="~/assets/home/logo.png" />
          <v-form>
            <v-text-field
              class="search-input"
              label="Search the web to plant trees..."
              solo
            ></v-text-field>
          </v-form>
          <h2>The search engine that plants trees.</h2>
          <h1><Counter/></h1>
          <p>Trees planted by Ecosia users.</p>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>
    <section class="countries-section">
      <v-row>
        <v-col cols="col-4"> </v-col>
        <v-col cols="col-4">
          <v-row>
            <v-col>
              <div>
                <h1 class="title uppercase">
                  Where are your trees being planted?
                </h1>
              </div>
              <div>
                <h3>We plant in 30+ countries with local organizations</h3>
              </div>
            </v-col>
          </v-row>
          <div class="countries-container">
            <v-row>
              <v-col cols="col-4">
                <v-row>
                  <v-col>
                    <img src="~/assets/home/brazil.webp" />
                  </v-col>
                </v-row>
                <v-row>
                  <v-col class="uppercase left-border"> Brazil </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    Your trees in Brazil protect thousands of endangered plants
                    and animals.
                  </v-col>
                </v-row>
              </v-col>
              <v-col cols="col-4">
                <v-row>
                  <v-col>
                    <img src="~/assets/home/burkinafaso.webp" />
                  </v-col>
                </v-row>
                <v-row>
                  <v-col class="uppercase left-border"> Burkina Faso </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    By planting trees in Burkina Faso, you restore desertified
                    land to its former fertility.
                  </v-col>
                </v-row>
              </v-col>
              <v-col cols="col-4">
                <v-row>
                  <v-col>
                    <img src="~/assets/home/indonesia.webp" />
                  </v-col>
                </v-row>
                <v-row>
                  <v-col class="uppercase left-border"> Indonesia </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    In Indonesia, your searches bring back forests on former
                    palm oil plantations while creating alternative sources of
                    income.
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </div>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>

    <section class="projects-section">
      <v-row>
        <v-col cols="col-4"></v-col>
        <v-col cols="col-4">
          <v-row>
            <v-col>
              <div>
                <h1 class="title uppercase">Trees planted by ecosia users</h1>
              </div>
              <div>
                <h1><Counter/></h1>
              </div>
            </v-col>
          </v-row>
          <v-row class="projects-container">
            <v-col cols="col-4" class="left-border">
              <div>15 Million</div>
              <div>People using Ecosia</div>
            </v-col>
            <v-col cols="col-4" class="left-border">
              <div>500+</div>
              <div>Native species</div>
            </v-col>
            <v-col cols="col-4" class="left-border">
              <div>30</div>
              <div>Countries</div>
            </v-col>
            <v-col cols="col-4" class="left-border">
              <div>60+</div>
              <div>Active projects</div>
            </v-col>
          </v-row>
          <v-row class="link-container">
            <a href="#">Discover our projects</a>
          </v-row>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>

    <section class="reports-section">
      <v-row>
        <v-col cols="col-4"></v-col>
        <v-col cols="col-4">
          <v-row>
            <v-col>
              <div>
                <h1 class="title uppercase">Monthly financial reports</h1>
              </div>
              <div>
                <h3>Our revenue in January 2022</h3>
              </div>
              <div>
                <h4 class="content">
                  Our monthly reports show how much ad revenue we made from your
                  searches, how we spent it, and how many trees this helped us
                  plant.
                </h4>
              </div>
            </v-col>
          </v-row>
          <v-row class="link-container">
            <a href="#">Explore our financial reports</a>
          </v-row>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>
    <section class="why-choose-us-section">
      <v-row>
        <v-col cols="col-4"></v-col>
        <v-col cols="col-4">
          <v-row>
            <v-col>
              <div>
                <h1 class="title uppercase">Why choose Ecosia?</h1>
              </div>
              <div>
                <h3>We put people and planet before profit</h3>
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="col-2">
              <img src="~/assets/home/profits.svg" />
            </v-col>
            <v-col cols="col-4">
              <div class="content">
                <p class="title">We’re a not-for-profit business</p>
                <p>
                  We dedicate 100% of our profits to climate action, with at
                  least 80% financing tree-planting projects.
                </p>
              </div>
            </v-col>
            <v-col cols="col-2">
              <img src="~/assets/home/privacy.svg" />
            </v-col>
            <v-col cols="col-4">
              <div class="content">
                <p class="title">Ecosia is powered by 200% renewable energy</p>
                <p>
                  Our solar panels produce twice the amount of energy needed to
                  power all searches with renewables.
                </p>
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="col-2">
              <img src="~/assets/home/world.svg" />
            </v-col>
            <v-col>
              <div class="content">
                <p class="title">We always put your privacy first</p>
                <p>
                  We anonymize your searches and don’t create a profile of you.
                  We’re interested in trees, not your data.
                </p>
              </div>
            </v-col>
            <v-col cols="col-2">
              <img src="~/assets/home/coin.svg" />
            </v-col>
            <v-col cols="col-4">
              <div class="content">
                <p class="title">We are transparent about everything we do</p>
                <p>
                  We publish detailed financial reports and frequent updates
                  from our tree planting projects.
                </p>
              </div>
            </v-col>
          </v-row>
          <v-row class="link-container">
            <a href="#">Other reasons</a>
          </v-row>
        </v-col>
        <v-col cols="col-4"></v-col>
      </v-row>
    </section>
    <section class="join-us-section">
      <v-row>
        <v-col cols="col-12">
          <div class="join-us-container">
            <h1>Join 15 million people who already use Ecosia!</h1>
            <v-btn color="primary"> Share Ecosia </v-btn>
          </div>
        </v-col>
      </v-row>
    </section>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style lang="scss" scoped>
$alice-blue: aliceblue;
$teal: teal;

.title {
  color: $teal;
}

.uppercase {
  text-transform: uppercase;
}

.left-border {
  border-left: 5px solid $teal;
}

.alice-blue {
  background-color: $alice-blue;
}

.link-container {
  display: flex;
  height: 5vh;
  justify-content: flex-end;
}

.search-engine-section {
  .search-engine-container {
    display: flex;
    height: 100vh;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  .search-input {
    width: 20vw;
    margin: 20px;
  }
}

.countries-section {
  background-color: $alice-blue;

  .countries-container {
    display: flex;
    height: 40vh;
    align-items: center;
    justify-content: center;
  }
}

.projects-section {
  .counter {
    font-size: 2em;
  }

  .projects-container {
    display: flex;
    height: 15vh;
    align-items: center;
    justify-content: center;
  }
}

.reports-section {
  background-color: $alice-blue;

  .content {
    max-width: 70%;
    padding: 30px 0px;
  }
}

.why-choose-us-section {
  .content {
    text-align: left;
  }
}

.join-us-section {
  background-color: $alice-blue;

  .join-us-container {
    display: flex;
    height: 15vh;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
}
</style>
