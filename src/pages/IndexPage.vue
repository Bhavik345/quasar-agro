<template>
  <q-page class="q-pa-md">
    <!-- Blue background with text on the left -->
    <div class="q-sm-xs bg-primary text-white q-gutter-sm">
      <div class="q-mb-md">
        <div class="row items-center">
          <h2 class="q-mb-sm text-caption">You are hero : /</h2>
          <h2 class="q-mb-sm text-caption">My Account /</h2>
          <h2 class="q-mb-sm text-caption">Upload Questions</h2>
        </div>
      </div>
    </div>

    <!-- Box with white text -->
    <div class="row items-center q-ma-md full-width justify-center">
      <div>
        <p class="text-black">
          Message Box: Recent updates are done on 01 Nov, 2023.
        </p>
      </div>
    </div>

    <!-- Space between sections -->
    <div class="q-mb-md"></div>

    <!-- Two dropdowns side by side -->
    <div class="row items-center q-mb-md">
      <div class="q-mr-md q-ml-md row items-center">
        <label for="frameworkTechnology">Technology/Framework:</label>
        <q-select
          id="frameworkTechnology"
          v-model="selectedTechnology"
          class="custom-width"
          :options="[
            { label: 'React', value: 'react' },
            { label: 'Angular', value: 'angular' },
            {
              label: 'Vue',
              value: 'vue',
            },
          ]"
        />
      </div>

      <div class="q-ml-md row items-center">
        <label for="difficulties">Filter The Questions:</label>
        <q-select
          id="difficulties"
          v-model="selectedDifficulty"
          class="custom-width"
          :options="[
            { label: 'Easy', value: 'easy' },
            { label: 'Medium', value: 'medium' },
            {
              label: 'Hard',
              value: 'hard',
            },
          ]"
        />
      </div>
    </div>

    <!-- Medium space -->
    <div class="q-mb-md"></div>

    <!-- Submit button -->
    <div class="text-center">
      <q-btn color="primary" class="custom-width" @click="submitForm"
        >Submit</q-btn
      >
    </div>

    <!-- Horizontal rule -->
    <hr class="q-mt-xl" />

    <!-- Space between sections -->
    <div class="q-mb-md"></div>

    <!-- Question and Answer section -->
    <div class="">
      <div class="q-mb-md">
        <p class="text-black">Question: What is lorem ipsum?</p>
      </div>
      <div class="q-mb-md">
        <p class="text-black">
          Answer: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        </p>
      </div>
    </div>

    <!-- Previous and Next buttons -->
    <div class="q-mx-auto text-center q-mt-xl">
      <q-btn color="primary" class="custom-width" @click="goToPrevious"
        >Previous</q-btn
      >
      <q-btn color="primary" class="custom-width q-ml-md" @click="goToNext"
        >Next</q-btn
      >
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  data() {
    return {
      selectedTechnology: null,
      selectedDifficulty: null,
    };
  },
  methods: {
    submitForm() {
      // Add your form submission logic here
      console.log("Form submitted!");
    },
    goToPrevious() {
      // Logic for going to the previous question
      console.log("Go to previous question");
    },
    goToNext() {
      // Logic for going to the next question
      console.log("Go to next question");
    },
  },
});
</script>

<style scoped>
.custom-width {
  width: 200px;
}
</style>
