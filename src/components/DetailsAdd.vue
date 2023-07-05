<template>
  <div class="p-4 w-96">
    <h1 class="text-2xl font-bold mb-4">Timetable Manager</h1>

    <h2 class="text-lg font-bold mb-2">Add Professor</h2>
    <form @submit.prevent="addProfessor">
      <div class="mb-4">
        <label class="block text-gray-700 font-bold mb-2" for="professor-name">
          Name
        </label>
        <input
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="professor-name" type="text" v-model="newProfessor.name">
      </div>
      <div class="mb-4">
        <label class="block text-gray-700 font-bold mb-2" for="professor-email">
          Email
        </label>
        <input
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="professor-email" type="email" v-model="newProfessor.email">
      </div>
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" type="submit">
        Add Professor
      </button>
    </form>

    <h2 class="text-lg font-bold my-4">Add Subject</h2>
    <form @submit.prevent="addSubject">
      <div class="mb-4">
        <label class="block text-gray-700 font-bold mb-2" for="subject-name">
          Name
        </label>
        <input
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="subject-name" type="text" v-model="newSubject.name">
      </div>
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" type="submit">
        Add Subject
      </button>
    </form>
    <h2 class="text-lg font-bold my-4">Assign Subject to Professor</h2>
    <form @submit.prevent="assignSubject">
      <div class="mb-4">
        <label class="block text-gray-700 font-bold mb-2" for="subject">
          Subject
        </label>

        <select
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="subject" v-model="selectedSubject">
          <option v-for="subject in subjects" :key="subject.id" :value="subject">{{ subject.name }}</option>
        </select>
      </div>
      <div class="mb-4">
        <label class="block text-gray-700 font-bold mb-2" for="professor">
          Professor
        </label>
        <select
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          id="professor" v-model="selectedProfessor">
          <option v-for="professor in professors" :key="professor.id" :value="professor">{{ professor.name }}</option>
        </select>
      </div>
    </form>
  </div>
</template>

<script>


export default {
  data() {
    return {
      newProfessor: {
        name: '',
        email: '',
      },
      newSubject: {
        name: '',
      },
      selectedSubject: null,
      selectedProfessor: null,
      subjects: [], // Provide your subjects data here
      professors: [], // Provide your professors data here
    };
  },
  methods: {
    addProfessor() {
      // Handle adding a new professor
    },
    addSubject() {
      // Handle adding a new subject
    },
    assignSubject() {
      // Handle assigning a subject to a professor
    },
  },
};



</script>