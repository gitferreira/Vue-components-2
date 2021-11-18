<template>
  <h2>My friends</h2>
  <ul>
<friend-contact></friend-contact>
<friend-contact></friend-contact>
  </ul>
</template>

<script>

export default {
  data() {
    return {
    FriendContacts: [
        {
          id: "Manu",
          name: "Manuel Ruiz",
          phone: "944609878",
          email: "banana@gmail.com",
        },
        {
          id: "Jules",
          name: "Jules Roy",
          phone: "944607438478",
          email: "banana1@gmail.com",
        },
      ],
    };
  },
};
</script>