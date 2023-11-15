<script setup>
import ModulesSection from "../components/landing/ModulesSection";
import FeaturesSection from "../components/landing/FeaturesSection";
import AOS from "aos";
import TestimonialsSection from "~~/components/landing/TestimonialsSection.vue";

onMounted(() => {
  AOS.init()
})
</script>

<template>
  <div class="relative">
    <div class="relative">
      <section class="relative w-full min-h-[96vh] mt-20">

        <div class="max-w-5xl mx-auto text-center px-5 lg:px-0">
          <h1 class="StaticGradientText text-6xl lg:text-7xl font-bold">
            Nostrocket
          </h1>
          <h2 class="text-3xl  lg:text-5xl font-bold dark:text-white px-4">
            The productive way to build fullstack Nuxt 3 applications.
          </h2>
          <h3 class="text-lg mt-8 text-gray-800 dark:text-gray-400">
            sidebase is a web app development kit to build production ready fullstack apps quickly. We build sidebase to provide a modular, modern, fully-typed and best-practice approach to make your ideas a reality. Around a core of TypeScript and Nuxt 3 sidebase adds components like Prisma ORM, tRPC, Authentication, CI, testing and more!
          </h3>
        </div>

        <div class="relative mx-auto flex items-center space-x-5 w-full justify-center mt-5 px-5 lg:px-0">
          <ButtonLink href="/sidebase/welcome">
            Learn More
          </ButtonLink>
          <NuxtLink href="https://github.com/sidebase/sidebase" target="_blank" class="text-gray-700 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white font-bold">
            Everthing on GitHub
          </NuxtLink>
        </div>

       
        
      </section>
      <section class="relative py-6" data-aos="fade-up">
        <div class="relative SidebaseContainer">
          <div class="Heading">
            <h1>
              Our amazing <span class="GradientTextPurple">modules</span>!
            </h1>
            <p>
              Together with our main starter, we focus on developing high quality, developer experienced oriented Nuxt 3 modules.
            </p>
          </div>
          <ModulesSection />
        </div>
      </section>
      <section class="relative py-6" data-aos="zoom-up">
       
        <div class="relative SidebaseContainer">
          <div class="Heading">
            <h1>
              What do others think of <span class="GradientText">sidebase</span>?
            </h1>
            <p>
              The opinions of the community matter a lot to us! Have a look at what other developers have said about sidebase.
            </p>
          </div>
          <TestimonialsSection />
        </div>
      </section>
      
    </div>
  </div>
</template>

<style scoped>
.Heading {
  margin: 100px 0 50px 0;
}

.Heading h1 {
  font-size: 3rem;
  font-weight: bold;
}

.Heading p {
  max-width: 50rem;
  font-size: 1.3rem;
}

.StaticGradientText {
  background: linear-gradient(to right, #81F6D4 10%, #12a87b 40%, #0FCF97 60%, #81F6D4 90%);
  background-size: 200% auto;
  background-position: 60% center;

  color: #000;
  background-clip: text;
  text-fill-color: transparent;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.GradientText {
  background: linear-gradient(to right, #7bceb6 10%, #12a87b 40%, #0FCF97 60%, #7bceb6 90%);
  background-size: 200% auto;

  color: #000;
  background-clip: text;
  text-fill-color: transparent;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;

  animation: shine 1s linear infinite;
  @keyframes shine {
    to {
      background-position: 200% center;
    }
  }
}

.GradientTextPurple {
  background: linear-gradient(to right, #95b4ab 10%, #8136d4 40%, #9881e6 60%, #95b4ab 90%);
  background-size: 200% auto;

  color: #000;
  background-clip: text;
  text-fill-color: transparent;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;

  animation: shine 1s linear infinite;
  @keyframes shine {
    to {
      background-position: 200% center;
    }
  }
}

.SpinAnimation {
  animation: linear 7000ms spin infinite;
  transform-origin: center 35% 0;
  filter: blur(80px);
  opacity: 75%;
}

@keyframes spin {
  from {
    transform:rotate(0deg);
  }
  to {
    transform:rotate(360deg);
  }
}
</style>