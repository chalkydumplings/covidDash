

<template>
  <div>
    <ul v-if="posts"> <!-- NOT GONNA LIE FELT LIKE A GENIUS FUCK YAH -->
      
        
        <h1> {{posts.summary[0]}}</h1>
    </ul>
    <h1> People fully Vaccinated Circle Graph </h1>

    <ul v-if="errors && errors.length">
      <li :v-for="error in errors">
        {{error.message}}
      </li>
    </ul>
  </div>
</template>

<script>
// think what I will do is CIRCLE GRAPH POPULATION OF CANADA vs PEOPLE Fully vaccinated
//
import axios from 'axios';

export default {
  data() {
    return {
      posts: [],
      errors: []
    }
  },

  // Fetches posts when the component is created.
  //this works actually AMAZING
  async created() {
    try {
      const response = await axios.get(`https://api.opencovid.ca`)
      this.posts = response.data
      console.log(response.data)
    } 
    
    catch (e) {
      this.errors.push(e)
    }
  }
}

</script>