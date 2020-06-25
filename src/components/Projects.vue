<template>
  <section id="projects">
            <h1>Projects</h1>
            <p> </p>
            <div class="container">
                <div class="row">
                    <div class="col-md-4 d-flex align-items-stretch">
                        <div class="card">
                            <div class="card-head">
                                <img alt="Vue logo" class="rounded-circle img-custome" src="https://cdn3.iconfinder.com/data/icons/gradient-3/50/229-512.png">
                                <h2>Personal Website</h2>
                            </div>
                            <hr>
                            <div class="card-body">
                                <p>
                                    What you're currently looking at! Built with VueJS and Bootstrap, it is a single page
                                    website featuring a responsive design and animations to create a seamless experience for the user.
                                </p>
                                <div class="btnDiv">
                                    <button type="button" class="btn btn-outline-secondary">
                                        <a href="https://github.com/eyturner/eyturner.github.io">Github</a>
                                    </button>
                                    <button type="button" class="btn btn-outline-secondary">
                                        <a href="#title">Demo</a>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4 d-flex align-items-stretch">
                        <div class="card">
                            <div class="card-head">
                                <img alt="Vue logo" class="rounded-circle img-custome" src="https://cdn2.iconfinder.com/data/icons/flaturici-set-4/512/rocket-512.png">
                                <h2>Missions</h2>
                            </div>
                            <hr>
                            <div class="card-body">
                                <p>
                                    A simple todo-list web application. It allows users to create Missions with TaskSets and Tasks and manages
                                    state using only VanillaJS and Webpack. Missions utilizes localStorage to ensure user's data is saved.
                                </p>
                                <div class="btnDiv">
                                    <button type="button" class="btn btn-outline-secondary">
                                        <a href="https://github.com/eyturner/Missions">Github</a>
                                    </button>
                                    <button type="button" class="btn btn-outline-secondary">
                                    <a href="https://eyturner.github.io/Missions/">Demo</a>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4 d-flex align-items-stretch">
                        <div class="card">
                            <div class="card-head">
                                <img alt="Vue logo" class="rounded-circle img-custome" src="https://cdn2.iconfinder.com/data/icons/data-science-7/512/data-science-lab-18-512.png">
                                <h2>Maze Algorithm Visualizer</h2>
                            </div>
                            <hr>
                            <div class="card-body">
                                <p>
                                    A web app designed to display multiple algorithms for generating mazes. The user can 
                                    control which algorithm is implemented as well as the speed at which it is implemented.
                                </p>
                                <div class="btnDiv">
                                    <button type="button" class="btn btn-outline-secondary">
                                        <a href="https://github.com/eyturner/MazeAlgorithmVisualizer/">Github</a>
                                    </button>
                                    <button type="button" class="btn btn-outline-secondary">
                                    <a href="https://eyturner.github.io/MazeAlgorithmVisualizer/">Demo</a>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4 d-flex align-items-stretch">
                        <div class="card">
                            <div class="card-head">
                                <img alt="Vue logo" class="rounded-circle img-custome" src="https://cdn0.iconfinder.com/data/icons/reports-and-analytics-5/128/3-512.png">
                                <h2>Border Crossing Analysis</h2>
                            </div>
                            <hr>
                            <div class="card-body">
                                <p>
                                    A project done as a challenge for Insight Data. Given a huge CSV file of border crossing data,
                                    aggregate it and return the data in a more user-friendly format with helpful data points.
                                </p>
                                <div class="btnDiv">
                                    <button type="button" class="btn btn-outline-secondary">
                                        <a href="https://github.com/eyturner/Border-Crossing-Analysis">Github</a>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                     <div class="col-md-4 d-flex align-items-stretch">
                        <div class="card">
                            <div class="card-head">
                                <img alt="Vue logo" class="rounded-circle img-custome" src="https://cdn2.iconfinder.com/data/icons/bee-farm-filled/64/bee_farm-20-512.png">
                                <h2>Buzzy Bee</h2>
                            </div>
                            <hr>
                            <div class="card-body">
                                <p>
                                    A web game modeled after NYT's Spelling Bee. Built in VanillaJS it features a 
                                    responsive page design and utilizes async/await methods to verify words with an online dictionary.
                                </p>
                                <div class="btnDiv">
                                    <button type="button" class="btn btn-outline-secondary">
                                        <a href="https://github.com/eyturner/BuzzingBee">Github</a>
                                    </button>
                                    <button type="button" class="btn btn-outline-secondary">
                                        <a href="https://eyturner.github.io/BuzzingBee/">Demo</a>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4 d-flex align-items-stretch">
                            <div class="card">
                                <div class="card-head">
                                    <img alt="Vue logo"
                                      class="rounded-circle img-custome" src="https://cdn1.iconfinder.com/data/icons/bots/280/bot-9-2-512.png">
                                    <h2>D&D Dice Roller Bot</h2>
                                </div>
                                <hr>
                                <div class="card-body">
                                    <p>
                                        A Discord bot written in NodeJS for my DnD group. This bot helps users roll dice as 
                                        well as keeps track of initiative rolls for the DM. It also features some secret commands 
                                        as a comedy component.
                                    </p>
                                    <div class="btnDiv">
                                        <button type="button" class="btn btn-outline-secondary">
                                            <a href="https://github.com/eyturner/DnD-Dice-Bot">Github</a>
                                        </button>
                                    </div>
                                </div>
                            </div>
                            <br>
                    </div>
                </div>
            </div>
        </section>
</template>

<style scoped>
    #projects{
        background-color: rgb(76,91,82);
        padding-top: 8%;
        padding-bottom: 15%;
        color: rgba(255, 255, 255, 0.87);
        min-height: 100vh; 
        padding: 5%;
        font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
    }
    .img-custome{
        width: 140px;
        height: 140px;
        margin-top: 15px;
    }

    .card {
        transition: ease-in-out 0.1s;
        background: rgb(29,35,41);
        border-radius: 5px;
        margin-bottom: 20px;
    }

    .card:hover {
        transform: scale(1.05);
        transition: ease-in-out 0.2s;
        box-shadow: 0 0 6px rgba(255, 255, 255, 0.87);
    }

    h1 {
        text-align: left;
        border-bottom: 3px solid rgb(50,58,66);
        width: 166px;
        margin-bottom: 5%;
        font-family: 'Titillium Web', sans-serif;
        font-weight: 800;
    }

    a{
        text-decoration: none;
        color: inherit;
    }

    .btn {
        margin: 5px 5px;
    }

    h2 {
        font-family: 'Titillium Web', sans-serif;
    }

    .card-body {
        display: flex;
        flex-direction: column;
        justify-content:space-between;
        height: 100%;
    }
</style>