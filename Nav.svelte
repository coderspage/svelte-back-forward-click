<script>

  import {page_shown} from "./data.js"

  const show_page = () =>{
    // console.log(event.target.getAttribute("href"))
    const url = event.target.getAttribute("href")
    history.pushState({"href_to_show":url}, '', url)
    $page_shown = url
  }

</script>


<nav>
  <a href="/" on:click|preventDefault={show_page}>home</a>
  <a href="about-us" on:click|preventDefault={show_page}>about us</a>
  <a href="contact-us" on:click|preventDefault={show_page}>contact us</a>
</nav>