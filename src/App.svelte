<script>
  import LandingPage from './components/LandingPage.svelte'
  import router from 'page'
  import CustomerCareCard from './components/CustomerCareCard.svelte'
  let page
  let querystring
  router('/', () => page = LandingPage)
  router('/customer-care-card', (ctx, next) => {
    querystring = ctx.querystring
    next()
  }, 
  () => page = CustomerCareCard)
  router.start()
</script>
<main>
  <svelte:component this={page} {querystring}/>
</main>