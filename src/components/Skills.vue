<template>
  <div id="skills">
    <h1>Skills</h1>
    <div class="skillDivs">
      <div class="skillSet" ref="swVisible">
        <h4>Software Development</h4>
        <div id="swLangs">
          <div class="swLang" :class="{'langSeen': swVisible}" v-for="lang in devLangs" :key="lang">
          {{ lang }}
        </div>
        </div>
      </div>
      <div class="skillSet">
        <h4>Software Tools</h4>
        <li v-for="tool in devTools" :key="tool" id="toolSet"> {{ tool }}</li>
      </div>
      <div class="skillSet" ref="langVisible">
        <h4>International Languages</h4>
        <div class="language" :class="{ 'animateOn': langVisible}">
          <h5>Spanish</h5>
          <li>Reading</li><span class="bar"><span v-if="langVisible" id="reading-sp"></span></span>
          <li>Writing</li><span class="bar"><span v-if="langVisible" id="writing-sp"></span></span>
          <li>Speaking</li><span class="bar"><span v-if="langVisible" id="speaking-sp"></span></span>
        </div>
        <div class="language" :class="{ 'animateOn': langVisible}">
          <h5>Japanese</h5>
          <li>Reading</li><span class="bar"><span v-if="langVisible" id="reading-jp"></span></span>
          <li>Writing</li><span class="bar"><span v-if="langVisible" id="writing-jp"></span></span>
          <li>Speaking</li><span class="bar"><span v-if="langVisible" id="speaking-jp"></span></span>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      devLangs: ['Python', 'Javascript', 'HTML5', 'CSS3', 'C++', 'NodeJS', 'Vue', 'BASH', 'Wolfram'],
      devTools: ['Express', 'Mongoose', 'Git', 'Github', 'NPM', 'Chrome DevTools', 'Boostrap', 'Jest'],
      langVisible: false,
      swVisible: false,
    }
  },

  mounted () {
    window.addEventListener('scroll', this.onScroll)
  },

  beforeDestroy () {
    window.removeEventListener('scroll', this.onScroll)
  },

  methods: {
    onScroll() {
      let langTop = this.$refs.langVisible.getBoundingClientRect().top;
      let swTop = this.$refs.swVisible.getBoundingClientRect().top;
      
      if(langTop < 660 && langTop > -350) {
        this.langVisible = true;
      }
      else {
        this.langVisible = false;
      }
      if(swTop < 660 && swTop > -350) {
        this.swVisible = true;
      }
      else {
        this.swVisible = false;
      }
      return;
    }
  }

}
</script>

<style scoped>
  #skills {
    padding: 5%;
    text-align: left;
    background: rgb(97,130,106);
    color: rgba(255, 255, 255, 0.87);
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  }

  h1 {
    border-bottom: 3px solid rgb(50,58,66);
    width: 116px;
    font-family: 'Titillium Web', sans-serif;
    font-weight: 800;
  }

  h4 {
    border-bottom: 2px solid rgb(50,58,66);
    font-family: 'Titillium Web', sans-serif;
  }

  .skillDivs {
    margin-top: 5%;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
  }

  .skillSet {
    text-align: center;
    padding: 15px;
    min-width: 200px;
    max-width: 300px;
  }

  #swLangs {
    display: flex;
    flex-wrap: wrap;
    justify-content:flex-start;
    margin-top: 25px;
  }

  .swLang {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 80px;
    width: 80px;
    border: 1px solid rgba(0, 0, 0, 0.0);
    border-radius: 50%;
    margin: 5px;
    padding: 10px;
    transition: ease-in-out 0.2s;
    font-size: 14px;
  }

  .langSeen {
    transition: 1s ease-in-out 0.2s;
    border: 1px solid rgba(0,0,0,0.315);
  }

  #toolSet {
    text-align: left;
    margin: 5% 0;
  }

  .language {
    text-align: left;
    display: flex;
    flex-direction: column;
    list-style: none;
    margin-top: 25px;
  }

  .bar {
    background: #47474752;
    display: block;
    height: 5x;
  }

  .bar span {
    height: 5px;
    float: left;
    background: rgba(184, 184, 144, 0.853);
    border-radius: 2px;
  }

  #reading-sp {
    width: 75%;
    animation: skillBar ease 1s;
  }
  #writing-sp {
    width: 60%;
    animation: skillBar ease 1s;
  }
  #speaking-sp {
    width: 35%;
    animation: skillBar ease 1s;
  }
  #reading-jp {
    width: 55%;
    animation: skillBar 1s;
  }
  #writing-jp {
    width: 40%;
    animation: skillBar 1s;
  }
  #speaking-jp {
    width: 25%;
    animation: skillBar 1s;
  }

  @keyframes skillBar {
    0% {
      width: 0;
    }
  }
  
</style>