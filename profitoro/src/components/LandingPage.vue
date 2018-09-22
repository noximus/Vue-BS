//LandingPage.vue
 <template>
  <div>
    <logo></logo>
    <tagline></tagline>
    <Authentication></Authentication>
    <go-to-app-link></go-to-app-link>
  </div>
</template>
<script>
  import {Authentication, GoToAppLink, Tagline} from './landing'
  import {Logo} from './common'
  export default {
    components: {
      Logo,
      Authentication,
      GoToAppLink,
      Tagline
    }
  }
</script>
<style>
  
</style>