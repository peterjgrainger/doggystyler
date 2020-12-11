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
      <img src="http://store.storeimages.cdn-apple.com/4044/as-images.apple.com/is/image/AppleInc/aos/published/images/H/D1/HD162/HD162?wid=800&hei=800&fmt=jpeg&qlt=95&op_sharpen=0&resMode=bicub&op_usm=0.5,0.5,0,0&iccEmbed=0&layer=comp&.v=1400749861094" alt="" class="details-img--ball"/>
    </div>
    <div class="col-7 details">
      <h3>Free Dog Report Cards</h3>
      <p>Customisable report cards you can print off and give to customers</p>
			 <a href="#" class="btn btn-transparent">Make yours now!</a>
    </div>
  </div>
</section>

<section class="section--primary--alt">
    <div class="col-12 text--center">
    <h3>Want to be the first to access new content?</h3>
		<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSeJIkSpIBr12HdlfnimV-j8-uhAtYU_uoojIeJnmnM_uuaI8A/viewform?embedded=true" width="400" height="638" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
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

.col-5 {
  width: 30%;
}
@media (max-width: 34.375em) {
  .col-5 {
    width: 60%;
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


@media (max-width: 43.75em) {
  .features {
    width: 100%;
    margin: 0;
    text-align: left;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2);
  }
}

@media (max-width: 43.75em) {
  .features i {
    font-size: 1.5rem;
    width: 2rem;
    text-align: center;
    margin: 0 0 1rem 0;
    float: left;
  }
}

@media (max-width: 43.75em) {
  .features p {
    margin-left: 3rem;
  }
}

blockquote {
  position: relative;
  margin: 0;
  padding: 0;
  text-align: center;
}
blockquote:before {
  display: inline-block;
  color: #007ece;
  font-size: 2rem;
  content: '\201C';
}

@media (max-width: 43.75em) {
  blockquote p {
    font-size: 1.2rem;
  }
}

@media (max-width: 43.75em) {
  blockquote cite {
    font-size: .8rem;
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