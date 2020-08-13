<template>
  <div class="core-rail container-with-shadow p0" role="main">
    <cv-header />
    <cv-achievements />

    <cv-experience />

    <cv-education />

    <!-- CV Skills section start -->
    <div v-if="skills.length > 0" class="cv-section skill-section">
      <div class="cv-section-inner">
        <h3>Skills</h3>

        <ul class="cv-section-list">
          <li v-for="skill in skills" :key="skill.id">
            <cv-skill :skill="skill" />
          </li>
        </ul>
      </div>
    </div>
    <!-- CV Skills section end -->

    <!-- CV Projects section start -->
    <!-- <div v-if="projects.length > 0" class="cv-section">
      <div class="cv-section-inner">
        <h3>Projects</h3>

        <ul class="pv-accomplishments-block__list pv-accomplishments-block__list--has-more">
          <cv-project v-for="project in projects" :key="project.id" :project="project" />
        </ul>
      </div>
    </div>-->
    <!-- CV Projects section end -->

    <!-- CV Licenses & Certifications section start -->
    <!-- <div v-if="certifications.length > 0" class="cv-section">
      <h3>Licenses &amp; certifications</h3>

      <ul>
        <cv-certification
          v-for="certification in certifications"
          :key="certification.id"
          :certification="certification"
        />
      </ul>
    </div>-->
    <!-- CV Licenses & Certifications section end -->
  </div>
</template>

<script>
import { Projects, Skills, Certifications } from "../data/data";
import CvHeader from "./CvHeader";
import CvAchievements from "./CvAchievements";
// import CvProject from "./CvProject";
import CvSkill from "./CvSkill";
import CvExperience from "./CvExperience";
import CvEducation from "./CvEducation";
// import CvCertification from "./CvCertification";
export default {
  name: "MyCv",
  components: {
    CvHeader,
    CvAchievements,
    // CvProject,
    CvSkill,
    CvExperience,
    CvEducation
    // CvCertification
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
<style lang="scss">
.cv-section {
  position: relative;
  overflow: hidden;
  padding: 0 30px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.15);

  &:last-of-type {
    margin-bottom: 48px;
    border-bottom: none;
  }

  .cv-section-inner {
    margin: 30px 0;

    h3 {
      font-size: 20px;
      line-height: 1;
      margin-bottom: 15px;
    }

    .cv-section-list {
      margin-left: 16px;

      li {
        font-size: 14px;
        line-height: 23px;
      }
    }
  }
}
</style>
