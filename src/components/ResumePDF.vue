<template>
  <div id="pdfDiv">
      <button type="button" class="btn" v-on:click="loadPDF('resume.pdf')">Full Resume Here</button>
  </div>
</template>

<script>
export default {
methods: {
  loadPDF(pdfFile) {
    window.open(process.env.BASE_URL + pdfFile);
  }
}
}
</script>

<style scoped>
  #pdfDiv{
    width: 100%;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgb(32,47,53);
  }

  button {
    font-size: 40px;
    transition: ease-in-out 0.4s;
    color: rgb(204, 204, 184);
  }

  button:hover {
    font-size: 42px;
    transition: ease-in-out 0.4s;
    background-color: rgb(53,66,73);
    color: rgb(204, 204, 184);
  }
</style>