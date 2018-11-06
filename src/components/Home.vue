<template>
  <div class="content">
      <div class="container">
        <img src="../assets/ravenland-logo.png" height="300px">
      </div>
      <div class="explanation back-blue">
        <div class="container">
          <h2 class="white section-title">What is RAVENLAND?</h2>
          <p class="white text">
            Ravenland is an experimental community ran and owned estate agent for the buying and selling of land and estate in individual ravenland slices.
            A free and open source project, like the Ravencoin community Ravenland is a unique and ambitious opportunity for the Ravencoin community to demonstrate the real utility of the Raven Core asset layer to solve a real problem as well as innovating a new crowd funded asset model.
          </p>
        </div>
      </div>
      <div class="explanation back-white">
        <div class="container">
          <p class="orange text">
            We want to use Ravencoin to sell slices of land or to transparently and seamlessly manage the co ownership of building assets using Raven signed digital blockchain keys, which assist both buyers in securing a share of larger assets and assists sellers in securing the liquidity of larger assets not usually purchasable by a single buyer instantly and online.
          </p>
          <p class="orange text">
            This we feel would give the market a much wider region of trading, create a fairer, more fluid market liquidity and grant the new ability to trade existential assets of physical worth digitally 24 hours and 7 days a week without restriction, overcoming all borders via the token asset model, something we do not believe has been done before, and something which we believe will go a long way to revolutionizing the estate and land assets industries.
          </p>
          <p class="orange text text-large">
            The middle men better watch closely or risk being left behind! <br> Welcome to RavenLand.
          </p>
        </div>
      </div>
      <div id="team" class="explanation back-blue">
        <div class="container team">
          <h2 class="white section-title small-padding">Meet our team</h2>
          <div class="columns is-multiline is-centered">
            <TeamMember 
              v-for="teamMember in teamMembers" 
              :member="teamMember"
              :class="columnClass" />
          </div>
        </div>
      </div>
      <div class="explanation back-white">
        <div class="container">
          <h2 class="orange section-title small-padding">Become a part of our community</h2>
          <p class="orange text no-margin">
            Learn more about RavenLand and join the discussion in our discord
          </p>
          <a href="https://discord.gg/3448yES"><img class="discord-logo" src="../assets/discord-join.png" height="60px"></a>
        </div>
      </div>
  </div>
</template>

<script>

// array containing all the team members
import TeamMembers from '../data/teammembers'
// TeamMember component
import TeamMember from  '../components/TeamMember'

export default {
  name: 'Home',
  components: {
    'TeamMember': TeamMember
  },
  data() {
    return {
      teamMembers: [],
    }
  },
  computed: {
    columnClass() {
      if (this.teamMembers.length > 4)
        return 'column is-half-tablet is-one-third is-centered'
      else
        return 'column is-half-tablet is-one-quarter is-centered'
    }
  },
  mounted() {
    this.teamMembers = TeamMembers;
  }
}
</script>

<style scoped>

.member-photo {
  padding: 0;
}

img {
  padding: 60px;
}

.text-large {
  font-size: 40px;
}

.explanation {
  padding: 40px;
}

.back-blue {
  background-color: #2e3e80;
}

.back-white {
  background-color: white;
}

.white {
  color: white;
}

.orange {
  color: #f15b22;
}

.section-title {
  font-size: 47px;
  font-weight: 400;
  padding: 20px;
}

.text {
  box-sizing: border-box;
  width: 80%;
  margin-left: 10%;
  line-height: 52px;
}

.small-padding {
  padding: 10px;
}

.no-margin {
  margin-top: 0px;
  margin-bottom: 0px;
}

.no-padding {
  padding: 0px;
}

.discord-logo {
  padding: 0px;
  padding-top: 20px;
}

.team {
  padding-bottom: 40px;
}

.columns {
    flex-wrap: wrap;
    align-items: stretch;
    justify-content: center;
}
</style>
