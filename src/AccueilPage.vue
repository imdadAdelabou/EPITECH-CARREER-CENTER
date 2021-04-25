<template>
    <div id="accueilPage">
        <div id="firstSection">
            <div class="header">
                <img src="./assets/logo_mobile-removebg-preview.png"/>
                <div class="rightElement">
                    <ul>
                        <li>Find Jobs</li>
                        <li>Browse Startup</li>
                    </ul>
                </div>
            </div>
            <h1>Find Your Dream Job</h1>
            <div id="searchBlock">
                <SearchComponent />
                <img src="./assets/publicdomainq-0006224bvmrqd.svg" id="laptop1"/>
            </div>
        </div>
        <div id="secondSection">
            <div class="leftBlock">
                <h3>Job Types</h3>
                <ul v-for="type in jobTypes" v-bind:key="jobTypes.indexOf(type)">
                    <li><TypeJob v-bind:content="type"/></li>
                </ul>
                <h3>Job Roles</h3>
                <ul v-for="role in jobRoles" v-bind:key="jobRoles.indexOf(role)">
                    <li><TypeJob v-bind:content="role"/></li>
                </ul> 
            </div>
            <div class="middleBlock">
                <ul v-for="job in jobs" v-bind:key="jobs.indexOf(job)">
                    <li>
                        <TitleJob v-bind:img="job.img" v-bind:name="job.name" v-bind:description="job.description"/>
                    </li>
                </ul>
            </div>
            <div class="rightBlock">
                <div id="mail">
                    <span class="title">Get new jobs alerts by email</span>
                    <input type="text" id="mailInput" placeholder="My email address"/>
                    <button>Activate</button>
                </div>
                <div id="recent">
                    <span class="title">My recent searches</span>
                    <div class="dataRecent">
                        <span id="location">Los Angeles, California</span>
                        <span id="nbrNew">2 new</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import SearchComponent from './components/SearchComponent.vue';
    import TypeJob from './components/TypeJob.vue';
    import TitleJob from './components/TitleJob.vue';
    export default {
        name: 'AccueilPage',
        data() {
            return {
                path: "",
                jobTypes: [
                    "Full-time",
                    "Part-time",
                    "Student",
                    "Internship",
                    "Freelance",
                ],
                jobRoles: [
                    "Design",
                    "IOS developer",
                    "Android Developer",
                    "Back-end Developer",
                    "Creative Director",
                    "Brand Designer"
                ],
                jobs: [
                    {
                        img: "",
                        name: "Flutter Developer",
                        description: "A junior flutter developer with \n1 or 2 years experience \nfor a salary between 120k or 220k euro.",
                    },
                    {
                        img: "./assets/c++.svg",
                        name: "C++ Developer",
                        description: "A c++ developer for a mission based on embedded systems.",
                    },
                    {
                        img: "./assets/py.png",
                        name: "Python Developer",
                        description: "A Python developer to help build a beautiful \nweb application using django and flask.",
                    }
                ],
            }
        },
        components: {
            SearchComponent,
            TypeJob,
            TitleJob,
        },
    }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
    #firstSection {
        width: 100%;
        height: 250px;
        background-color: #27346b;
        padding: 0px 20px 0px 20px;
    }
    .header img {
        width: 90px;
        height: 90px;
    }
    .header li {
        display: inline;
        font-size: 20px;
        color: white;
        padding: 0px 20px 0px 0px;
    }
    .header .rightElement {
        float: right;
        padding-right: 50px;
    }
    #firstSection h1 {
        color: white;
        font-family: 'Poppins';
        font-size: 50px;
        padding-left: 50px;
        margin: 10px 0px 0px 0px;
    }
    #laptop1 {
        width: 150px;
        height: 150px;
        margin-top: -50px;
    }
    #searchBlock {
        display: flex;
        margin-left:10%;
    }
    #secondSection {
        margin: 50px 0px 0px 50px;
        display: flex;
    }
    .leftBlock {
        float: left;
        box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        width: 15%;
        height: 100%;
        border-radius: 10px;
    }
    ul {
        list-style-type: none;
    }
    .leftBlock h3{
        font-family: "Poppins";
        margin-left: 30px;
    }
    .rightBlock {
        float: right;
        margin-right: 40px;
    }
    #mail {
        box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        border-radius: 10px;
        width: 200px;
        height: 150px;
        margin-bottom: 30px;
    }
     .title {
        font-size: 14px;
        padding-left: 10px;
        color: grey;
    }
    #mailInput {
        margin: 20px 10px 0px 10px;
        height: 30px;
        border-radius: 8px;
        border:1px solid #db5669;
        outline: none;
    }
    #mail button {
        width: 100px;
        height: 40px;
        background-color: #db5669;
        color: white;
        border-radius: 5px;
        border: none;
        outline: none;
        cursor: pointer;
        margin: 20px 0px 30px 10px;
    }
    #recent {
        width: 200px;
        height: 150px;
        border-radius: 10px;
        box-shadow: 0px 5px 15px rgba(0,0,0,0.3);
    }
    .dataRecent {
        margin: 10px 5px 0px 12px;
    }
    #location {
        float: left;
        font-size: 10px;
    }
    #nbrNew {
        float: right;
        font-size: 13px;
        color: #db5669;
    }
    .middleBlock {
        width: 800px;
        height: 500px;
        box-shadow: 0px 5px 15px rgba(0,0,0,0.3);
        margin: 0px 50px 0px 50px;
        border-radius: 20px;
    }
</style>