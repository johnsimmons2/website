<template>
  <div class="main-container">
    <h1 class="skill-header">Related technologies</h1>
    <div class="skills-container">
      <div v-if="!loaded">
        Hi there! I'm still fetching this data. Please wait while I load.
      </div>
      <div v-else v-for="(skill, id) in skills" :key="id">
        <div
          class="skills-obj"
          :style="{ 'background-image': 'url(' + getImgUrl(skill.name) + ')' }"
          @mousedown="setActive(id)"
          @mouseleave="setActive(-1)"
        >
          <div class="skill-description" v-if="activeId === id" @mouseover.stop>
            {{ skill.description }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      skills: {},
      loaded: {
        default: false,
        type: Boolean,
      },
      activeId: {
        default: -1,
        type: Boolean,
      },
    };
  },
  methods: {
    getSkills() {
      this.$http
        .get('skills.json')
        .then(function(data) {
          this.skills = data.body;
          this.loaded = true;
          console.log(this.skills);
        })
        .catch(function(err) {
          console.log(err);
        });
    },
    getImgUrl(name) {
      return '/assets/' + name.replace(/[\s\\.]/, '').toLowerCase() + '.png';
    },
    setActive(id) {
      this.activeId = id;
    },
  },
  mounted: function() {
    this.getSkills();
  },
};
</script>

<style scoped>
.skill-description {
  background-color: var(--js-primary-soft);
  color: var(--js-white);
  font-weight: 500;
  border-radius: 4px;
  position: absolute;
  height: 10rem;
  width: 20rem;
  box-shadow: 5px 7px 7px rgba(0, 0, 0, 0.6);
  padding: 12px;
}

.main-container {
  display: grid;
  grid-template-columns: 2fr 5fr 1fr;
  justify-items: center;
}

.skill-header {
  height: 36%;
  text-align: center;
  background-color: var(--js-primary-soft);
  grid-row: span 1;
  color: var(--js-white);
  box-shadow: 5px 7px 7px rgba(0, 0, 0, 0.6);
  padding: 16px 8px;
  word-break: break-word;
  border-radius: 4px;
  margin-left: 50px;
}

.skills-container {
  grid-row: span 2;
  margin: auto;
  width: 100%;
  background-color: var(--js-primary);
  display: grid;
  gap: 2rem;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  justify-items: center;
  padding: 50px;
  border-radius: 4px;
  box-shadow: 5px 7px 7px rgba(0, 0, 0, 0.6);
}

.skills-obj {
  background-color: var(--js-white);
  background-size: cover;
  justify-self: center;
  border-radius: 4px;
  padding: 12px;
  transition: 180ms;
  width: 140px;
  height: 140px;
}

.skills-obj:hover {
  transform: scale(1.05);
  cursor: pointer;
  box-shadow: 5px 7px 7px rgba(0, 0, 0, 0.6);
}
</style>
