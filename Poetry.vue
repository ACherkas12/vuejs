<template>
  <div class="poetry">
      <div class="placeholder-form">
        <div class="placeholder-container">
          <input type="text" placeholder=" " />
          <label>Enter the title of the poem</label>
        </div>
      </div>
      <div class="poetry-lines" v-for="value in poetry" :key="value.poetry">
        <div class="poetry-lines_author">
          <h3 class="poetry-lines_title">
            {{ value.title }}
          </h3>
        </div>
        <div class="poetry-lines_lines" >
         <p> {{ value.lines}} </p>
      </div>
    </div>
    </div>


</template>

<script lang="ts">
import axios from 'axios'

export default {
  name: 'Poetry',
  data() {
    return {
      poetry: [],
      errors: []
    }
  },
  created() {
    axios.get('https://poetrydb.org/title/Ozymandias/lines.json')
    .then(responce => {
      this.poetry = responce.data.lines[0]
      console.log(responce)
    })
    .catch(e=> {
      this.errors.push()
    })
  }
}

</script>