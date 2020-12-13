<script>
  import LandingPage from './components/LandingPage.svelte'
  import router from 'page'
  import CustomerCareCard from './components/CustomerCareCard.svelte'
  let page

  router('/', () => page = LandingPage)
  router('/customer-care-card', () => page = CustomerCareCard)
  router.start()
</script>
<main>
  <svelte:component this={page} />
</main>