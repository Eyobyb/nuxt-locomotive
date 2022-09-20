<template>
  <div class="w-screen py-14 bg-primary text-white p-5 flex justify-center items-center">
    <div class="flex flex-col gap-8 px-10 max-w-[1300px] w-full">
      <div class="flex flex-col md:flex-row items-center gap-5">
        <img
          src="../../assets/images/my-pic.JPG"
          class="w-32 h-36 object-cover object-top rounded-[19px]"
          alt
        />
        <p
          class="font-bold font-fam-raleway text-4xl md:text-7xl text-center p-1"
        >Let’s Work Together</p>
      </div>
      <div class="flex flex-col md:flex-row gap-5 items-center">
        <primay-button :brightBorder="true">eyobyirgu@gmail.com</primay-button>
        <primay-button :brightBorder="true">+251937112506</primay-button>
      </div>
      <div class="overflow-hidden">
        <svg
          width="1380"
          height="2"
          viewBox="0 0 1380 2"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M0 1L1380 0.999879" stroke="#505050" />
        </svg>
      </div>
      <div class="flex gap-20 items-end">
        <div class="flex flex-col gap-3">
          <p class="text-customGray font-Raleway font-thin">VERSION</p>
          <p class="text-white font-Raleway font-medium">2022 Edition</p>
        </div>

        <div class="flex gap-12">
          <SocialIcon>
            <img src="../../assets/Icons/cssbattle.svg" alt />
          </SocialIcon>
          <SocialIcon>
            <img src="../../assets/Icons/discord.svg" alt />
          </SocialIcon>
          <SocialIcon>
            <img src="../../assets/Icons/facebook.svg" alt />
          </SocialIcon>
          <SocialIcon>
            <img src="../../assets/Icons/instegram.svg" alt />
          </SocialIcon>
          <SocialIcon>
            <img src="../../assets/Icons/linkedin.svg" alt />
          </SocialIcon>
          <SocialIcon>
            <img src="../../assets/Icons/telegram.svg" alt />
          </SocialIcon>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PrimayButton from '../../components/PrimayButton.vue'
import SocialIcon from '../../components/SocialIcon.vue'
export default {
  components: { PrimayButton, SocialIcon }
}
</script>