<template>
  <div id="nav" ref="nav">
    <div id="navFlex" :class="{'showNav' : pastTitle}">
      <div class="navbarItem">
        <a href = "#about">
          <span>About</span>
          <span class="dot" :class="{'isActive' : currSection == 2}"></span>
        </a>
      </div>
      <div class="navbarItem">
        <a href = "#projects">
          <span>Projects</span>
          <span class="dot" :class="{'isActive' : currSection == 3}"></span>
        </a>
      </div>
      <div class="navbarItem">
        <a href = "#skills">
          <span>Skills</span>
          <span class="dot" :class="{'isActive' : currSection == 4}"></span>
        </a>
      </div>
      <div class="navbarItem">
        <a href = "#work">
          <span>Work</span>
          <span class="dot" :class="{'isActive' : currSection == 5}"></span>
        </a>
      </div>
      <div class="navbarItem">
        <a href = "#pdfDiv">
          <span>Resume</span>
          <span class="dot" :class="{'isActive' : currSection == 6}"></span>
        </a>
      </div>
    </div>  
  </div>
</template>

<script>
export default {
  data() {
    return {
      pastTitle: false,
      currSection: -1,
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
      const bottom = document.documentElement.scrollHeight;
      const HEIGHT = window.innerHeight;
      const BUFFER = 10; //Number of pixels from bottom to trigger
      
      if(bottom - currentScrollPos < HEIGHT + BUFFER) {        
        this.currSection = 6;
        return;
      }
      
      // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
      
      if (currentScrollPos < 550) {
        this.pastTitle = false;
        return;
      } else {
        this.pastTitle = true;
        let sections = this.$refs.nav.parentElement.childNodes
        let sectionTops = this.getSectionTops(sections);
        this.setCurrentSection(sectionTops, HEIGHT);
        return;
      }
    },

    getSectionTops(sections) {
      let sectionTops = [];
      for(let i = 0; i < sections.length; ++i) {
          sectionTops.push(sections[i].getBoundingClientRect().top);
        }        
      return sectionTops;
    },

    setCurrentSection(sectionTops, HEIGHT) {
      let nextSection = -1;
      for(let i = 0; i < sectionTops.length; i++) {     
        if (sectionTops[i] < HEIGHT/2) {
          nextSection = i; // 2: About, 3: Skills, 4: Projects, 5: Work, 6: Resume
        }        
        if (nextSection > 0) {
          this.currSection = nextSection;
        }
      }
    }
  }
}
</script>


<style lang="css" scoped>
  #nav {
    position: fixed;
    top: 30%;
    right: 0;
    height: 200px;
    width: 100px;
    transition: ease-in-out 0.2s;
    color: rgba(204, 204, 184,0.87);
    z-index: 1;
    font-family: 'Montserrat', sans-serif;
    padding-right: 2%;
    transition: ease 0.2s;
  }

  #navFlex {
    height: 200px;
    width: 80px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: flex-end;
    opacity: 0;
    transition: ease 0.2s;
  }

  .showNav {
    opacity: 1 !important;
    transition: 0.2s ease;
  }

  .navbarItem {
    display: inline-flex;
    height: 40px;
    justify-content: center;
    align-items: center;
  }

  a {
    font-size: 14px;
    color: transparent;
    transition: 0.1s;
  }

  a:hover {
    text-decoration: none;
    color: rgb(240, 238, 219);
  }

  a:hover .dot {
    transform: scale(1.2);
  }

  .dot {
    height: 12px;
    width: 12px;
    background: rgba(200,200,200,0.8);
    border: 1px solid rgba(200,200,200,0);
    border-radius: 50%;
    display: inline-block;
    margin-left: 5px;
    transition: ease 0.15s;
  }

  .isActive {
    background: rgba(14, 95, 27, 0.822);
    transition: ease 0.15s;
  }

  .dotLink {
    display: inline-block;
  }

</style>
