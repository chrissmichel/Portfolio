<template>
  <div class="profile">
    <div class="profile-header">
      <div class="profile-text">
        <h1>Christian Michel</h1>
        <h2>Computer Science Student and Aspiring Developer</h2>
        <span class="location"><svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <circle cx="12" cy="12" r="10"></circle>
                                <path d="M12 2a14.5 14.5 0 0 0 0 20 14.5 14.5 0 0 0 0-20"></path>
                                <path d="M2 12h20"></path>
                            </svg> Lancaster Pennsylvania, United States </span> 
        <div class="profile-links">
          <a href="#">Resume</a> | <a href="#">Cover Letter</a> 
        </div>
        <div class="contact-icons">
          <a :href="'mailto:' + email" aria-label="My Email"><i class="fas fa-envelope"></i></a>
          <a :href="'tel:' + phone" aria-label="My Phone Number"><i class="fas fa-phone"></i></a>
          <a :href="linkedin" aria-label="LinkedIn Profile"><i class="fab fa-linkedin"></i></a>
          <a :href="github" aria-label="GitHub Profile"><i class="fab fa-github"></i></a>
        </div>
      </div>
      <img :src="getImageUrl()" alt="Profile Picture" class="profile-image">
    </div>
  </div>
  
</template>

<script>
export default {
  name: 'Profile',
  data() {
    return {
      email: "christianmichelPA@gmail.com",
      phone: "717-224-7562",
      linkedin: "https://www.linkedin.com/in/christian-michel-a5602b293/",
      github: "https://github.com/hihi4605"
    };
  },
  methods: {
    getImageUrl() {
      return new URL('../assets/picture.jpeg', import.meta.url).href;
    }
  }
};
</script>

<style src="../style.css"></style>
