<template>
  <li>
    <h2>{{ name }} {{ friendIsFavourite ? "(Fav)" : "" }}</h2>
    <button @click="toggleFavourite">Toggle Fav</button>
    <button @click="toggleDetails">
      {{ detailsAreVisible ? "Hide" : "Show" }} Details
    </button>
    <ul v-if="detailsAreVisible">
      <li>Phone: {{ phoneNumber }}</li>
      <li>Email: {{ emailAddress }}</li>
    </ul>
  </li>
</template>

<script>
export default {
  // props: ["name", "phoneNumber", "emailAddress", "isFavourite"],
  props: {
    name: {
      type: String,
      required: true,
    },
    phoneNumber: {
      type: String,
      required: true,
    },
    emailAddress: {
      type: String,
      required: true,
    },
    isFavourite: {
      type: Boolean,
      required: false,
      default: false,
      // validator: function(value) {
      //   return value === '1' || value === '0'
      // }
    },
  },
  data() {
    return {
      detailsAreVisible: false,
      // friend: {
      //   id: "Manu",
      //   name: "Manuel Ruiz",
      //   phone: "944609878",
      //   email: "banana@gmail.com",
      // },
      friendIsFavourite: this.isFavourite,
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
    toggleFavourite() {
      this.friendIsFavourite = !this.friendIsFavourite;
    },
  },
};
</script>
