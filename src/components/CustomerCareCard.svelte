<script>
import Dog from './Dog.svelte'


  export let querystring;
  let pageContent = {
    businessName : 'Doggy Styler',
    terms : 'In signing this card I understand the above named pet is left at my own risk. In an emergency, if a vet is required during the grooming process, the cost will be payable by me. I have read, understand and agree to these terms.'
  }

  function separateQueryString() {
      (querystring || '').split('&')
                         .map(queryParameter => queryParameter.split('='))
                          .forEach(element => {
                              pageContent[element[0]] = element[1]
                          });
  };

  separateQueryString()

  function copyLinkText() {
    /* Get the text field */
    var copyText = `${document.location.host}${document.location.pathname}?businessName=${pageContent.businessName}&terms=${pageContent.terms}`
    // Create new element
    var el = document.createElement('textarea');
    // Set value (string to be copied)
    el.value = copyText;
    // Set non-editable to avoid focus and move outside of view
    el.setAttribute('readonly', '');
    el.style = {position: 'absolute', left: '-9999px'};
    document.body.appendChild(el);
    // Select text inside element
    el.select();
    // Copy text to clipboard
    document.execCommand('copy');
    // Remove temporary element
    document.body.removeChild(el);
}

function print() {
  window.print()
}

</script>
<div class="full-page">
<div class="logo">
  <a href="/">
  <Dog/>
  Doggy Styler
  </a>
</div>
<header class="share-link center">
  <div class="container">
    <h1>Customer Care Card</h1>
    <h3>(works best printing A5 landscape, business name and terms can be changed)</h3>
    <h2> 
      <button class="btn btn-transparent" on:click={copyLinkText}>Copy Link</button>
      <button class="btn btn-transparent" on:click={print}>Print</button></h2>
  </div>
</header>

<div class="margin-box">

<div class="bg-image">
  <h1>
    {#if pageContent.businessName}
      <input bind:value={pageContent.businessName} minlength="1" maxlength="15">
    {/if}
  </h1>
  <h2>Customer Care Card</h2>
</div>

<div class="content-container">
  <form class="half">
    <h2>Owners Information</h2> 
    <div class="form-row">
      <div><p>Owner:&nbsp;&nbsp;&nbsp;</p></div>
      <div class="signature-line"/>
    </div>
    <div class="form-row">
      <div><p>Address:&nbsp;</p></div>
      <div class="signature-line"/>
    </div>
    <div class="form-row">
      <div><p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p></div>
      <div class="signature-line"/>
    </div>
  </form>
  <form class="half">
      <div class="form-row">
        <div><p>&nbsp;</p></div>
      </div>
      <div class="form-row">
        <div><p>Telephone:&nbsp;</p></div>
        <div class="signature-line"/>
      </div>
      <div class="form-row">
        <div><p>Vets&nbsp;Name:&nbsp;</p></div>
        <div class="signature-line"/>
      </div>
      <div class="form-row">
        <div><p>Vets&nbsp;Tel:&nbsp;</p></div>
        <div class="signature-line"/>
      </div>
  </form>
</div>



<div class="content-container bg-image-info">
    <div class="thirty-percent">
      <h2>Pet Information</h2>
      <div class="form-row">
        <div><p>Name:&nbsp;</p></div>
        <div class="signature-line"/>
      </div>
      <div class="form-row">
        <div><p>Colour:&nbsp;</p></div>
        <div class="signature-line"/>
      </div>
      <div class="form-row">
        <div><p>Behaviour:&nbsp;</p></div>
        <div class="signature-line"/>
      </div>
    </div>
    <div class="thirty-percent">
      <h2></h2>
      <div class="form-row">
        <div><p>Age:&nbsp;</p></div>
        <div class="signature-line"/>
      </div>
      <div class="form-row">
        <div><p>Breed:&nbsp;</p></div>
        <div class="signature-line"/>
      </div>
      <div class="form-row">
        <div><p>Sex:&nbsp;</p></div>
        <div class="signature-line"/>
      </div> 
    </div>
  <form class="thirty-percent">
    <h2>Medical History</h2>
    <div class="form-row">
      <p>Allergies:&nbsp;</p>
      <div class="signature-line"/>
    </div>
    <div class="form-row">
      <p>Vaccinated:&nbsp;</p>
      <div class="signature-line"/>
    </div>
    <div class="form-row">
      <p>Spayed:&nbsp;</p>
      <div class="signature-line"/>
    </div>
  </form>
</div>

<div class="content-container">
  <p class="language">
    <textarea> { pageContent.terms } </textarea></p>

</div>
<div class="content-container">
  <div class="signature">
    <div class="signature-line">
      <p>
        Owner's Signature:
      </p>
    </div>
    <div class="date-line">
    </div>
  </div>
</div>

</div>

</div>

<style>

.logo {
    display: none;
  }

@media(min-width: 43.75em) {
  .logo {
    display: block;
    width: 5em;
    text-align: center;
  }
}


header h1 {
  font-size: 3rem;
  /* margin: 0 0 1rem; */
}
@media (max-width: 43.75em) {
  header h1 {
    font-size: 2rem;
  }
}


.container {
  margin: 0 auto;
  width: 90%;
  max-width: 900px;
}

@media print {
  .share-link {
    display: none;
  }
}

.margin-box {
    margin-top: 4em;

    
  }

@media print {
  .margin-box {
    margin-top: 0em;
  }
}

@media (min-width: 43.75em) {
  .margin-box {
    margin: 4em 4em 4em 4em;
    border-width:0.5px; 
    border-style:solid;
  }
}



textarea { 
        width:100%; 
    } 
  * {
  box-sizing: border-box;
}

.full-page {
  font-family: roboto;
}

h1 {
  display: block;
  font-size: 2em;
  margin-block-start: 0em;
  margin-block-end: 0em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  font-weight: bold;
}

div {
  margin-block-start: auto;
}

h2 {
  display: block;
  font-size: 1.5em;
  margin-block-start: 0em;
  margin-block-end: 0em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  font-weight: bold;
}

p {
  margin-block-end: 0em;
  font-size: 0.9em;
}

.content-container {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  margin: 10px 0;
}



.thirty-percent {
  flex: 0 1 30%;
  display: flex;
  height: 100%;
  max-width: 30%;
  flex-wrap: wrap;
  align-items: flex-start;
}

.half {
  flex: 0 1 50%;
  display: flex;
  height: 100%;
  max-width: 50%;
  flex-wrap: wrap;
  align-items: flex-start;
}


.language {
  display: flex;
  width: 95%;
  margin: 0;
}

.form-row {
  display: flex;
  width: 98%;
  margin: 2px 0;
}
.signature {
  display: flex;
  flex-wrap: nowrap;
  width: 95%;
}
.signature p {
  margin: 10px 0 0;
}
.signature-line {
  justify-content: flex-start;
  width: 70%;
  border-bottom: 0.5px solid black;
}
.date-line {
  justify-content: flex-start;
  width: 30%;
  border-bottom: 0.5px solid black;
}


.bg-image {
  background: rgb(255,255,255);
  background: -moz-linear-gradient(127deg, rgba(255,255,255,1) 0%, rgba(241,241,250,1) 49%);
  background: -webkit-linear-gradient(127deg, rgba(255,255,255,1) 0%, rgba(241,241,250,1) 49%);
  background: linear-gradient(127deg, rgba(255,255,255,1) 0%, rgba(241,241,250,1) 49%);
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#ffffff",endColorstr="#f1f1fa",GradientType=1);
  position: relative;
  z-index: 1;
  overflow: hidden;
  text-align: cen;
}

.center{
  text-align: center;
}

.bg-image-info {
  background: rgb(255,255,255);
  background: -moz-linear-gradient(127deg, rgba(255,255,255,1) 0%, rgba(241,241,250,1) 49%);
  background: -webkit-linear-gradient(127deg, rgba(255,255,255,1) 0%, rgba(241,241,250,1) 49%);
  background: linear-gradient(127deg, rgba(255,255,255,1) 0%, rgba(241,241,250,1) 49%);
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#ffffff",endColorstr="#f1f1fa",GradientType=1);  position: relative;
  z-index: 1;
  overflow: hidden;
}

input {
  border-top-style: hidden;
  border-right-style: hidden;
  border-left-style: hidden;
  border-bottom-style: hidden;
  background: rgba(0, 0, 0, 0);
  padding: 0;
  margin: 0;
}

textarea {
  border-top-style: hidden;
  border-right-style: hidden;
  border-left-style: hidden;
  border-bottom-style: hidden;
  background: rgba(0, 0, 0, 0);
  padding: 0;
  margin: 0;
  overflow: auto;
  resize: none;
  height: 3.5em;
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



</style>