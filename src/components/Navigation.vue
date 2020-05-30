<template>
  <div id="nav" :class = "{ 'navbar-scroll' : !topNavbar }">
    <div class="navbarItem">
      <a href = "#about" :class = "{ 'visibleLink' : !visibleLink }">About</a>
    </div>
    <div class="navbarItem">
      <a href = "#skills" :class = "{ 'visibleLink' : !visibleLink }">Skills</a>
    </div>
    <div class="navbarItem">
      <a href = "#projects" :class = "{ 'visibleLink' : !visibleLink }">Projects</a>
    </div>
    <div class="navbarItem">
      <a href = "#work" :class = "{ 'visibleLink' : !visibleLink }">Work</a>
    </div>
    <div class="navbarItem">
      <a href = "#" :class = "{ 'visibleLink' : !visibleLink }" data-toggle="modal" data-target=".bd-example-modal-lg">Contact</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      topNavbar: true,
      visibleLink: true,
      lastScrollPos: 0,
    }
  },
  mounted () {
    window.addEventListener('scroll', this.onScroll)
  },

  beforeDestroy () {
    window.removeEventListener('scroll', this.onScroll)
  },

  methods: {
    onScroll () {
      // Get the current scroll position
      const currentScrollPos = window.pageYOffset || document.documentElement.scrollTop
      // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
      if (currentScrollPos < 550) {
        this.topNavbar = true;
        this.visibleLink = true;
        return;
      } 
      // Stop executing this function if the difference between
      // current scroll position and last scroll position is less than some offset
      else if (Math.abs(currentScrollPos - this.lastScrollPos) < 60) {
        return;
      }
      this.topNavbar = currentScrollPos > this.lastScrollPos;
      this.visibleLink = this.topNavbar;
      this.lastScrollPos = currentScrollPos;
    }
}
}
</script>


<style lang="css" scoped>
  #nav {
    position: fixed;
    top: 0;
    left: 0;
    height: 50px;
    width: 100%;
    transition: ease-in-out 0.2s;
    color: rgba(204, 204, 184,0.87);
    visibility: hidden;
    z-index: 1;
    font-family: 'Montserrat', sans-serif;
  }

  .navbarItem {
    display: inline-flex;
    height: 50px;
    justify-content: center;
    align-items: center;
    width: 20%;
  }

  a {
    font-size: 18px;
    color: inherit;
    visibility: hidden;
    transition: 0.1s;
  }

  a:hover {
    transform: scale(1.05);
    text-decoration: none;
    color: rgb(240, 238, 219);
  }

  .visibleLink {
    visibility: visible !important;
    transition: 0.15s;
  }

  .navbar-scroll {
    background: rgb(23,29,34);
    transition: ease-in-out 0.2s;
    color: rgba(255, 255, 255, 0.87) !important;
    visibility: visible !important;
  }

  #navFlex {
    display: flex;
    align-items: center;
    height: 50px;
  }

</style>