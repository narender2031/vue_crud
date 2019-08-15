<template>
  <div class="about mt-5">
    <h1>About Us</h1>
    <about-content :info="info"></about-content>
    <project-info :projects="projects"></project-info>
  </div>
</template>

<script>
import AboutContent from "../components/About";
import ProjectInfo from "../components/Projects";

export default {
  components: {
    AboutContent,
    ProjectInfo
  },
  data() {
    return {
      info: {
        name: "Narender Singh",
        email: "narender2031@gmail.com"
      },
      projects: [
        {
          title: "Human Resource Project",
          desc:
            "This Project Relate to the HR softwares. It help HR to manage their records and other works",
          id: 1
        },
        {
          title: "Personal Management Project",
          desc:
            "This Project helps to track your growth in any field. It gives you analytics what you learn and how it is good for you.",
          id: 2
        }
      ]
    };
  }
};
</script>
