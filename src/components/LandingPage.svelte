<script>
  import Dog from './Dog.svelte'
</script>
<main>
<header class="bg-image">
	
  <div class="container">
	<Dog/>
    <h1>dog grooming resources</h1>

  </div>
</header>

<section class="">
  <div class="container">
    <div class="col-3 text--center">
      <img src="customer-care-card.png" alt="" class="details-img--ball"/>
    </div>
    <div class="col-7 details">
      <h3>Free Customer Care Card</h3>
      <p>Report cards you can print off and give to customers</p>
			 <a href="/customer-care-card" class="btn">Print yours now!</a>
    </div>
  </div>
</section>

<section class="section--primary--alt">
    <div class="col-12 text--center">
    <h3>Want to be the first to access new content?</h3>
		<iframe id="big-form" src="https://docs.google.com/forms/d/e/1FAIpQLSeJIkSpIBr12HdlfnimV-j8-uhAtYU_uoojIeJnmnM_uuaI8A/viewform?embedded=true" width="640" height="638" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
		<iframe id="small-form" src="https://docs.google.com/forms/d/e/1FAIpQLSeJIkSpIBr12HdlfnimV-j8-uhAtYU_uoojIeJnmnM_uuaI8A/viewform?embedded=true" width="350" height="638" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
  </div>
</section>
</main>

<style>

@import url("//maxcdn.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.min.css");
@import url(//fonts.googleapis.com/css?family=Open+Sans:400,700,800,300);
* {
  box-sizing: border-box;
}

main {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

#small-form {
	display: none
}



@media (max-width: 43.75em) {
  #small-form {
		display: inline;
	}

	#big-form {
		display: none;
	}
	
}

a {
  text-decoration: none;
}
a:hover {
  text-decoration: none;
}

img {
  max-width: 100%;
}

.btn {
  display: inline-block;
  margin: 1rem 0;
  color: white;
  font-weight: 500;
  font-size: 1.3rem;
  background: #007ece;
  letter-spacing: .02em;
  border: none;
  border-radius: 5px;
  padding: .8rem 1rem .9rem;
  text-shadow: 0 1px rgba(0, 0, 0, 0.3);
  box-shadow: 0 0 2px rgba(0, 0, 0, 0.2);
}
@media (max-width: 43.75em) {
  .btn {
    padding: .5rem .7rem .6rem;
    font-size: 1rem;
  }
}
.btn:hover {
  background: #008ee8;
  color: #fff;
}
.btn:focus, .btn:active, .btn:focus:active {
  background: #006eb5;
  border-color: #006eb5;
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.5) inset;
}

.container {
  margin: 0 auto;
  width: 90%;
  max-width: 900px;
}

header {
  color: white;
  background: #007ece;
  padding: 5rem 0;
  text-align: center;
  position: relative;
  z-index: 1;
  overflow: hidden;
}
@media (max-width: 43.75em) {
  header {
    padding: 2rem 0;
  }
}
header h1 {
  font-size: 3rem;
  margin: 0 0 1rem;
}
@media (max-width: 43.75em) {
  header h1 {
    font-size: 2rem;
  }
}

section {
  background: #fff;
  color: #1c262b;
  padding: 3.5rem 0;
}
@media (max-width: 43.75em) {
  section {
    padding: 2rem 0;
  }
}

section.section--primary--alt {
  background: #27a4f4;
  color: #fff;
}

section h3 {
  text-align: center;
  font-size: 2rem;
  font-weight: 300;
  margin: 0 0 1rem;
}
@media (max-width: 43.75em) {
  section h3 {
    font-size: 1.5rem;
  }
}

section p {
  font-size: 1.2rem;
  font-weight: 300;
}

.col-7, .col-3 {
  margin: 0 1.5%;
  display: inline-block;
  vertical-align: top;
}

.col-7 {
  width: 64%;
}
@media (max-width: 43.75em) {
  .col-7 {
    width: 100%;
    margin: 0;
  }
}

.col-3 {
  width: 29%;
}
@media (max-width: 43.75em) {
  .col-3 {
    width: 100%;
    margin: 0;
  }
}

.details {
  text-align: left;
}
.details h3 {
  font-size: 2rem;
  text-align: left;
}

@media (max-width: 43.75em) {
  .details-img--ball {
    height: 200px;
    width: auto;
    margin: 0 auto;
  }
}


.text--center {
  text-align: center;
}

.bg-image {
  background: #007ece;
  text-align: center;
  position: relative;
  z-index: 1;
  overflow: hidden;
}
.bg-image:before {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  background: #333;
  background-size: cover;
  background-attachment: fixed;
  -webkit-filter: blur(5px);
          filter: blur(5px);
  opacity: .8;
  -webkit-transform: scale(1.1);
          transform: scale(1.1);
}

</style>