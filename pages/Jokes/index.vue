<template>
  <div>
      jokes
  </div>
</template>

<script>
import axios from 'axios'

export default {
    data() {
      return {
        jokes: []
      }
    },
    async created() {
      const configObj = {
        headers: {
          'Accept': 'application/json'
        }
      }

      try {
        const result = await axios.get('https://icanhazdadjoke.com/search', configObj)

        this.jokes = result.data
        console.log(result.data)
      } catch (error) {
        console.log('ze error', error)
      }

      

    },
    head(){
        return {
            title: 'Ze Dad Jokes',
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    content: 'Best place for shitty dad jokes'
                }
            ]
        }
    }
}
</script>

<style>

</style>