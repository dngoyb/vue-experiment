<template>
  <div class="projects">
    <h1 class="subheading grey--text">Projects</h1>
    <v-container class="my-5">
      <v-expansion-panel>
        <v-expansion-panel-content v-for="project in myProjects" :key="project.title">
          <div slot="header">{{project.title}}</div>
          <v-card>
            <v-card-text>
              <div class="font-weight-bold">due by {{project.due}}</div>
              <div>{{project.content}}</div>
            </v-card-text>
          </v-card>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Design a new website",
          person: "Ngoy Banza",
          due: "1st Jan 2019",
          status: "complete",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt quo sed tempore, voluptas veritatis provident nam aspernatur iure corrupti aliquid! Hic aut eos cumque, ullam aperiam fuga veniam nesciunt voluptates!"
        },
        {
          title: "Graphic designer",
          person: "Kamona Kalenga",
          due: "1st Jan 2019",
          status: "ongoing",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt quo sed tempore, voluptas veritatis provident nam aspernatur iure corrupti aliquid! Hic aut eos cumque, ullam aperiam fuga veniam nesciunt voluptates!"
        },
        {
          title: "Create community forum",
          person: "Muzo Sakabab",
          due: "1st Feb 2019",
          status: "overdue",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt quo sed tempore, voluptas veritatis provident nam aspernatur iure corrupti aliquid! Hic aut eos cumque, ullam aperiam fuga veniam nesciunt voluptates!"
        },
        {
          title: "Run 60 kilometers in March",
          person: "Mbang Ndondj",
          due: "3rd March 2019",
          status: "ongoing",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt quo sed tempore, voluptas veritatis provident nam aspernatur iure corrupti aliquid! Hic aut eos cumque, ullam aperiam fuga veniam nesciunt voluptates!"
        },
        {
          title: "Run 60 kilometers in March",
          person: "Ngoy Banza",
          due: "3rd March 2019",
          status: "ongoing",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt quo sed tempore, voluptas veritatis provident nam aspernatur iure corrupti aliquid! Hic aut eos cumque, ullam aperiam fuga veniam nesciunt voluptates!"
        }
      ]
    };
  },
  computed: {
    myProjects() {
      return this.projects.filter(project => {
        return project.person === "Ngoy Banza";
      });
    }
  }
};
</script>
