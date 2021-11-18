<template>
<div class="ui card">
  <div class="image">
    <img src="/images/avatar2/large/kristy.png">
  </div>
  <div class="content">
    <a class="header">Kristy</a>
    <div class="meta">
      <span class="date">Joined in 2013</span>
    </div>
    <div class="description">
      Kristy is an art director living in New York.
    </div>
  </div>
  <div class="extra content">
    <a>
      <i class="user icon"></i>
      22 Friends
    </a>
  </div>
</div>
</template>

<script>
 <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
export default {
    props: {
        usernamme: {
            type: String,
            required: true
        }
    },
    data() {
        return {
            user: {

            }
        }
    },

   async created() {
      const response =  await xios.get(`https://api.github.com/users/${this.usernamme}`)

      this.user = response
    }
};
</script>