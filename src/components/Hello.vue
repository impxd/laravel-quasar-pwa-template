<template>
  <div class="hello">
    <h5>Laravel 5.5 (as API) + Quasar PWA</h5>
    <ul>
      <li><a href="http://quasar-framework.org" target="_blank" rel="noopener">Docs</a></li>
      <li><a href="http://forum.quasar-framework.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://gitter.im/quasarframework/Lobby" target="_blank" rel="noopener">Gitter Chat</a></li>
      <li><a href="https://twitter.com/quasarframework" target="_blank" rel="noopener">Twitter</a></li>
    </ul>
    <br>
    <div>
      <p>Make an api request to Laravel <i>/api/test</i><br>
        <sub>Before you need to run <i>artisan serve</i></sub>
      </p>
      <q-btn loader :color="color" @click="makeRequest">
        make an api request
      </q-btn>
      <br><br>
      <code>
        {{response}}
      </code>
    </div>
  </div>
</template>

<script>
import {QBtn} from 'quasar'

export default {
  name: 'hello',
  data () {
    return {
      color: 'primary',
      response: ''
    }
  },
  methods: {
    async makeRequest (ev, done) {
      this.response = ''

      let response = 'request error'
      let color = 'negative'
      let req = await fetch('/api/test')

      if (req.ok) {
        let {data} = await req.json()
        response = data
        color = 'positive'
      }

      setTimeout(() => {
        this.response = response
        this.color = color
        done()
      }, 700)
    }
  },
  components: {
    QBtn
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus">
@import '~variables'

.hello
  margin-top 50px
  a
    color #35495E

ul
  list-style-type none
  padding 0

li
  display inline-block
  margin 0 10px
</style>
