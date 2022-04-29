<template>
  <div class="min-h-screen relative flex flex-col items-center justify-center">
    <img
      data-aos="zoom-in"
      class="animate__animated animate__bounceInDown neon h-72 rounded-full border-2 border-purple-800"
      src="../assets/lennyroland.jpg"
      alt="Portrait photo de Lenny Roland"
    />
    <div class="text-center mt-16 z-20 text-white text-2xl font-mono uppercase">
      Lenny ROLAND
    </div>
    <router-link
      to="portfolio"
      class="animate__animated animate__zoomInDown px-7 py-5 cursor-pointer hover:bg-purple-900 rounded-md animate__delay-2s mt-24 bg-purple-800 text-white"
    >
      Portfolio
    </router-link>

    <div class="absolute bottom-5 flex">
      <a
        href="https://instagram.com/shotxlejeu?igshid=YmMyMTA2M2Y="
        class="mx-2 animate__animated animate__heartBeat animate__delay-3s"
      >
        <img src="../assets/instagram.png" alt="" />
      </a>
      <a
        href="https://www.linkedin.com/in/lenny-roland-6a82a31b8/"
        class="mx-2 animate__animated animate__heartBeat animate__delay-4s"
      >
        <img src="../assets/linkedin.png" alt="" />
      </a>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "HomeView",
};
</script>
