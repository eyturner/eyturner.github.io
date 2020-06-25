<template>
  <div id="work">
    <h1>Experience</h1>
    <div class="timelineBody">
    <main>
      <p data-date='2015'><strong>Student Manager, Bert's Cafe</strong><br>Lead shifts of up to six employees, including keeping employees on task, fixing errors, and running the employee of the month program. Kept inventory of all baked goods and ordered new stock when needed.</p>
      <p data-date='2018'><strong>Student Research Assistant, Plasmadynamics and Electric Propulsion Laboratory</strong><br>Assisted in tests of vaccuum chamber by designing and fabricating a waterfall board to reduce systematic error due to wire tension. Reduced the chance of electric arcing by building nylon thimbles to replace standard electrical tape.</p>
      <p data-date='2018'><strong>University of Michigan</strong><br>Graudated with a B.S.E in Engineering Physics with a focus of Aerospace Engineering and a Minor in Mathematics.</p>
      <p data-date='2019'><strong>Front Desk Staff, Bridges Rock Gym</strong><br>Ensured proper opening of gym, including facility maintenance, cleaning, and preparation for events. Handled customer service requests including membership agreements, customer complaints, and event coordination. Voted “Most Valuable Desk Staff” of 2019 by managers of the gym.</p>
      <p data-date='2020'><strong>The Odin Project</strong><br>Completed the Full-Stack Javascript Course offered by The Odin Project which included completing over 300 hours of work and 25+ projects.</p>
    </main>
  </div>
  </div>
</template>

<style lang="scss" scoped>
//Text Styles 

//Colors
$black: #34435E;

.timelineBody {
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  margin: 0;
  padding: 0 4em;
  color: rgba(255, 255, 255, 0.87);
}

#work {
  padding: 5%;
  background-image:
    linear-gradient(to bottom, rgba(180, 180, 180, 0.52), rgba(0, 0, 0, 0.83)),
    url('../assets/timelineImage.png');
  
  min-height: 100vh;

  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

main {
  min-width: 200px;
  max-width: 500px;
  margin: auto;
}

h1 {
  text-align: left;
  border-bottom: 3px solid rgb(50,58,66);
  width: 216px;
  color: rgba(255, 255, 255, 0.87);
  font-family: 'Titillium Web', sans-serif;
  font-weight: 800;
}

p {
  font-size: 1em;
  line-height: 1.75em;
  border-top: 3px solid;
  border-image: linear-gradient(to left, #157c15 0%, #15178a 100%);
  border-image-slice: 1;
  border-width: 3px;
  margin: 0;
  padding: 40px;
  position: relative;
  color: rgb(240, 238, 219);
  
  //numbers
  &:before {
    content: attr(data-date);
    position: absolute;
    border-radius: 50%;
    padding: 10px;
    padding-top: 18px;
    padding-left: 9px;
    height: 3.5em;
    width: 3.5em;
    background-color: $black;
    line-height: 1.25em;
    color: rgb(240, 238, 219);
    font-size: 1em;
  }
}
//odd number borders
p:nth-child(odd) {
  border-right: 3px solid;
  padding-left: 0;
  border-left: 0px solid;
  
  &:before {
    left: 100%; 
    margin-left: -27px;
  }
}
//even number borders
p:nth-child(even) {
  border-left: 3px solid;
  padding-right: 0;
  border-right: 0px solid;
  
  &:before {
    right: 100%; 
    margin-right: -27px;
  }
}
//handle first and last
p:first-child {
  border-top: 0;
  border-top-right-radius:0;
  border-top-left-radius:0;
}
p:last-child {
  border-bottom-right-radius:0;
  border-bottom-left-radius:0;
}

strong {
  font-size: 18px;
}
</style>