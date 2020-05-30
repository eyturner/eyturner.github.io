<template>
  <div id = 'about'>
    <div id="writeup">
      <h1>Nice to meet you!</h1>
      <br>
      <h3>I'm a full-stack engineer with a physics background interested in using engineering to help as many people as possible.</h3>
      <div id="about-text">
        <p><strong>I recently graduated from The University of Michigan</strong> with a degree in Physics and a Minor in Mathematics. However I have a deep love of programming that traces back to making games with my dad in visual basic. 
        Since graduating, I have delved deep into the world of web development and dabbled in many areas. I've written programs ranging from a Secret Santa script for my work to a D&D Dice Bot for my discord group, to a word puzzle based on the New York Time's Spelling Bee.</p>
        <p>However, my favorite aspect of coding is the unprecedented ability to reach a large-scale audience. Because of this I feel the best use for my software abilities is to help as many people as I can. </p>
        <p>When I'm not coding, you'll find me playing tennis, practicing piano, learning Japanese, and rock climbing.</p>
      </div>
    </div>
    <div id="photo">
      <img id = "mypic" alt="Vue logo" class="rounded-circle" src="https://avatars0.githubusercontent.com/u/11673130?s=460&u=da7de5497ecccd9e4e0a18e497a40569f21c910c&v=4">
    </div>
  </div>
</template>

<style scoped>
  #about {
    display: flex;
    min-height: 100vh; 
    justify-content: space-around;
    background: rgb(32,48,49);
    color: rgba(255, 255, 255, 0.87);
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
  }
  #writeup {
    min-height: 100%;
    flex-grow: 9;
    display: flex;
    flex-direction: column;
    align-items: stretch;
    min-width: 430px;
    padding: 6%;
    padding-right: 1%;
    text-align: left;
    margin: 0 6px;
  }

  @media only screen and (max-width: 820px) {
    #about {
      flex-wrap: wrap;
    }

    #photo {
      order: 1;
    }

    #about-text {
      order: 2;
    }
    #writeup {
      order: 3;
    }
  }


  #photo {
    min-height: 100%;
    flex-grow: 7;
    display: flex;
    align-items: center;
    margin-right: 3%;
    justify-content: center;
  }

  #mypic {
    transform: scale(0.75);
  }

  #about-text {
    margin-top: 10%;
    display: flex;
    justify-content: flex-start;
    text-align: left;
    font-size: 18px;
    flex-direction: column;
  }

  h1, h3{
    font-family: 'Titillium Web', sans-serif;
  }
</style>