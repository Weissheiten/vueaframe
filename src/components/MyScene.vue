<template>
  <div>
    <a-scene>

      <a-plane position="0 -2 -5" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-entity v-for="(skill,index) in skills" :key="skill.id" id="color" :position="{x:0,y:index*0.1,z:-4}" :text="{color: black, align: center, width: 1.5, value: skill.title}">

      </a-entity>

    </a-scene>
  </div>
</template>

<script>
  import {SkillDisplay} from '@/services/SkillDisplay';

export default {
  name: 'MyScene',
  props: {
    msg: String
  },
  data(){
    return {
      skills: []
    }
  },
  created(){
    let sd = new SkillDisplay();
    sd.getSkillSet(108).then(response => {
      console.log(response)
      this.skills = response.skills;
    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
