<template>
  <div class="w-4/5 block mx-auto p-4 border-b mb-6 text-white">
    <h2 class="text-xl font-bold">John C. Robson</h2>
    <h3 class="text-base">Development Portfolio</h3>
    <div class="flex flex-row gap-2">
      <a
        href="https://www.linkedin.com/in/john-robson-63a294289/"
        class="w-20 px-2 py-1 bg-slate-200 rounded hover:bg-slate-400"
        target="_blank"
        ref="noopenner noreferrer"
        ><img src="./assets/LinkedIn.png"
      /></a>
      <a
        href="https://github.com/john-c-robson"
        class="w-20 px-2 py-1 bg-slate-200 rounded hover:bg-slate-400"
        target="_blank"
        ref="noopenner noreferrer"
        ><img src="./assets/GitHub.png"
      /></a>
    </div>
  </div>
  <div
    class="grid md:grid-cols-3 sm:grid-cols-2 gap-4 container w-4/5 mx-auto bg-neutral-800"
  >
    <PortfolioStub
      v-for="project in projects"
      :key="project.title"
      :title="project.title"
      :image="project.image"
      :url="project.url"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import PortfolioStub from "./components/PortfolioStub.vue";
import { Project } from "@/interfaces";
import pneumonia from "@/assets/cnnModelsImage.png";
import gestureclassification from "@/assets/GestureDetection.png";
import traffictracker from "@/assets/traffictracker.jpg";
import gradepredictor from "@/assets/gradepredictor.png";
import malariadetection from "@/assets/malariadetection.png";
import surveyrobot from "@/assets/surveyrobot.jpeg";

export default defineComponent({
  name: "App",
  components: {
    PortfolioStub,
  },
  setup() {
    const projects = ref<Project[]>([
      {
        title: "Pneumonia Detection",
        image: pneumonia,
        url: "https://github.com/john-c-robson/pneumoniadetection",
      },
      {
        title: "Gesture Classification",
        image: gestureclassification,
        url: "https://github.com/john-c-robson/gestureclassification",
      },
      {
        title: "Traffic Tracker",
        image: traffictracker,
        url: "https://github.com/john-c-robson/traffictracker",
      },
      {
        title: "Grade Predictor",
        image: gradepredictor,
        url: "https://github.com/john-c-robson/gradepredictor",
      },
      {
        title: "Malaria Model, Hyper Parameter Tuning",
        image: malariadetection,
        url: "https://github.com/john-c-robson/MalariadetectionHyperparametertuning",
      },
      {
        title: "Self Driving Surveying Robot",
        image: surveyrobot,
        url: "https://github.com/john-c-robson/selfdrivingsurveyingrobot",
      },
    ]);
    return { projects };
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

html,
body,
#app {
  background: #262626;
}
</style>
