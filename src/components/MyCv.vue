<template>
  <div class="core-rail container-with-shadow p0" role="main">
    <cv-header />
    <cv-achievements />

    <cv-experience />

    <cv-education />

    <!-- CV Skills section start -->
    <div v-if="skills.length > 0" class="cv-section skill-section">
      <h3 class="t-18 t-black t-bold">Skills</h3>
      <div class="t-14 t-black pv4">
        <cv-skill v-for="skill in skills" :key="skill.id" :skill="skill" />
      </div>
    </div>
    <!-- CV Skills section end -->

    <!-- CV Projects section start -->
    <div v-if="projects.length > 0" class="cv-section">
      <h3 class="t-18 t-black t-bold">Projects</h3>

      <ul
        class="pv-accomplishments-block__list pv-accomplishments-block__list--has-more"
      >
        <cv-project
          v-for="project in projects"
          :key="project.id"
          :project="project"
        />
      </ul>
    </div>
    <!-- CV Projects section end -->

    <!-- CV Licenses & Certifications section start -->
    <div v-if="certifications.length > 0" class="cv-section">
      <h3 class="t-18 t-black t-bold">Licenses &amp; certifications</h3>

      <ul>
        <cv-certification
          v-for="certification in certifications"
          :key="certification.id"
          :certification="certification"
        />
      </ul>
    </div>
    <!-- CV Licenses & Certifications section end -->
  </div>
</template>

<script>
import { Projects, Skills, Certifications } from "../data/data";
import CvHeader from "./CvHeader";
import CvAchievements from "./CvAchievements";
import CvProject from "./CvProject";
import CvSkill from "./CvSkill";
import CvExperience from "./CvExperience";
import CvEducation from "./CvEducation";
import CvCertification from "./CvCertification";
export default {
  name: "MyCv",
  components: {
    CvHeader,
    CvAchievements,
    CvProject,
    CvSkill,
    CvExperience,
    CvEducation,
    CvCertification
  },
  data() {
    return {
      projects: [],
      skills: [],
      experience: [],
      certifications: []
    };
  },
  mounted() {
    this.$nextTick(() => {
      this.projects = Projects;
      this.skills = Skills;
      this.certifications = Certifications;
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.cv-section {
  position: relative;
  padding: 0 15px;
  margin-bottom: 15px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.15);

  &:last-of-type {
    margin-bottom: 48px;
    border-bottom: none;
  }
}
</style>
