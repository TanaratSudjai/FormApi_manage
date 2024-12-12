<template>
  <div
    class="bg-gray-100 min-h-screen flex items-center justify-center py-12 px-4 sm:px-6 lg:px-8"
  >
    <div class="max-w-md w-full bg-white shadow-lg rounded-xl p-8 space-y-8">
      <div class="text-center">
        <h1 class="text-3xl font-extrabold text-gray-900">Add New Employee</h1>
        <p class="mt-2 text-sm text-gray-600">
          Fill out the form to register a new team member
        </p>
      </div>
      <form @submit.prevent="submitForm" class="space-y-6">
        <div>
          <label
            htmlFor="name"
            className="block text-sm font-medium text-gray-700"
            >Name</label
          >
          <input
            type="text"
            id="name"
            v-model="form.name"
            required
            className="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500"
          />
        </div>

        <div>
          <label
            htmlFor="email"
            className="block text-sm font-medium text-gray-700"
            >Email</label
          >
          <input
            type="email"
            id="email"
            v-model="form.email"
            required
            className="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500"
          />
        </div>

        <div>
          <label
            htmlFor="password"
            className="block text-sm font-medium text-gray-700"
            >Password</label
          >
          <input
            type="password"
            id="password"
            v-model="form.password"
            required
            className="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500"
          />
        </div>

        <div className="grid grid-cols-2 gap-4">
          <div>
            <label
              htmlFor="age"
              className="block text-sm font-medium text-gray-700"
              >Age</label
            >
            <input
              type="number"
              id="age"
              v-model="form.age"
              required
              className="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500"
            />
          </div>

          <div>
            <label
              htmlFor="hireDate"
              className="block text-sm font-medium text-gray-700"
              >Hire Date</label
            >
            <input
              type="date"
              id="hireDate"
              v-model="form.hireDate"
              required
              className="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500"
            />
          </div>
        </div>

        <div>
          <label
            htmlFor="position"
            className="block text-sm font-medium text-gray-700"
            >Position</label
          >
          <select
            id="position"
            v-model="form.position"
            required
            className="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500"
          >
            <option value="developer">Developer</option>
            <option value="designer">Designer</option>
            <option value="manager">Manager</option>
          </select>
        </div>

        <div>
          <label className="block text-sm font-medium text-gray-700"
            >Gender</label
          >
          <div className="mt-1 space-x-4">
            <label className="inline-flex items-center">
              <input
                type="radio"
                value="male"
                v-model="form.gender"
                className="form-radio h-4 w-4 text-indigo-600"
              />
              <span className="ml-2">Male</span>
            </label>
            <label className="inline-flex items-center">
              <input
                type="radio"
                value="female"
                v-model="form.gender"
                className="form-radio h-4 w-4 text-indigo-600"
              />
              <span className="ml-2">Female</span>
            </label>
          </div>
        </div>

        <div>
          <label className="block text-sm font-medium text-gray-700"
            >Skills</label
          >
          <div className="mt-1 grid grid-cols-2 gap-2">
            <label className="inline-flex items-center">
              <input
                type="checkbox"
                value="JavaScript"
                v-model="form.skills"
                className="form-checkbox h-4 w-4 text-indigo-600"
              />
              <span className="ml-2">JavaScript</span>
            </label>
            <label className="inline-flex items-center">
              <input
                type="checkbox"
                value="Vue.js"
                v-model="form.skills"
                className="form-checkbox h-4 w-4 text-indigo-600"
              />
              <span className="ml-2">Vue.js</span>
            </label>
            <label className="inline-flex items-center">
              <input
                type="checkbox"
                value="Node.js"
                v-model="form.skills"
                className="form-checkbox h-4 w-4 text-indigo-600"
              />
              <span className="ml-2">Node.js</span>
            </label>
            <label className="inline-flex items-center">
              <input
                type="checkbox"
                value="CSS"
                v-model="form.skills"
                className="form-checkbox h-4 w-4 text-indigo-600"
              />
              <span className="ml-2">CSS</span>
            </label>
          </div>
        </div>

        <div>
          <label
            htmlFor="profileImage"
            className="block text-sm font-medium text-gray-700"
            >Profile Image</label
          >
          <input
            type="file"
            id="profileImage"
            @change="handleFileChange"
            className="mt-1 block w-full text-sm text-gray-500 file:mr-4 file:py-2 file:px-4 file:rounded-full file:border-0 file:text-sm file:bg-indigo-50 file:text-indigo-700 hover:file:bg-indigo-100"
          />
        </div>

        <div>
          <button
            type="submit"
            className="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          >
            Add Employee
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: "",
        email: "",
        password: "",
        age: null,
        hireDate: "",
        position: "",
        gender: "",
        isActive: false,
        skills: [],
        profileImage: null,
      },
    };
  },
  methods: {
    handleFileChange(event) {
      this.form.profileImage = event.target.files[0];
    },
    async submitForm() {
      try {
        const formData = new FormData();
        for (const key in this.form) {
          formData.append(key, this.form[key]);
        }
        console.log(this.form);

        // Uncomment and adjust API endpoint as needed
        // const response = await this.$axios.post(
        //   "http://localhost:5000/api/add",
        //   formData,
        //   {
        //     headers: {
        //       "Content-Type": "multipart/form-data",
        //     },
        //   }
        // );
      } catch (error) {
        console.error(error);
        alert("Failed to add employee");
      }
    },
  },
};
</script>
