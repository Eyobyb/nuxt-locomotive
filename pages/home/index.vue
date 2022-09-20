<template>
  <main>
    <!-- <SectionHero />  -->
    <SmoothScroll>
      <hero />
      <about />
      <!-- <SectionSpace /> -->
      <!-- <SectionItemLeft />
      <SectionItemRight />
      <SectionItemLeft />
      <SectionItemRight />
      <SectionItemLeft />
      <SectionItemRight />
      <SectionItemLeft />-->
      <!-- <SectionSpace /> -->
      <Footer />
    </SmoothScroll>
    <CursorFollower />
  </main>
</template>

<script>
import SectionHero from './SectionHero'
import SectionSpace from './SectionSpace'
import SectionItemLeft from './SectionItemLeft'
import SectionItemRight from './SectionItemRight'
import SmoothScroll from '~/components/SmoothScroll'
import CursorFollower from '~/components/CursorFollower'
import Hero from '../Hero/Hero.vue'
import About from '../../components/About.vue'
import Footer from '../footer/Footer.vue'

export default {
  components: {
    SectionHero,
    SectionSpace,
    SectionItemLeft,
    SectionItemRight,
    SmoothScroll,
    CursorFollower,
    Hero,
    About,
    Footer
  },

  data() {
    return {
      scroll: null
    }
  },

  head() {
    return {
      title:
        this.$config.app.title +
        this.$config.app.titleSeparator +
        this.$config.app.titleTemplate,

      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.$config.app.description
        }
      ]
    }
  },

  mounted() {
    this.locomotiveScrollInit()
    this.setHeroAnimation()
    this.setItemAnimation()
  },

  beforeDestroy() {
    this.scroll.destroy()
  },

  methods: {
    locomotiveScrollInit() {
      this.scroll = new this.$LocomotiveScroll({
        el: document.querySelector('[data-scroll-container]'),
        smooth: true,
        getDirection: true
      })

      this.scroll.stop()
    },

    setHeroAnimation() {
      const ease = 0.05
      const star = document.querySelector('[data-img-star]')

      const onComplete = () => {
        this.scroll.update()
        this.scroll.start()

        this.scroll.on('scroll', instance => {
          star.style.transform = `rotate(${instance.scroll.y * ease}deg)`
        })
      }

      const tl = this.$gsap.timeline({
        defaults: { duration: 3, ease: 'expo.out' }
      })

      tl.to('[data-svg-title]', {
        y: 0,
        opacity: 1
      }).to(
        '[data-img-star]',
        {
          opacity: 1,
          scale: 1,
          rotation: 360,
          transformOrigin: '50% 50%',
          onComplete
        },
        '-=2.5'
      )
    },

    setItemAnimation() {
      this.scroll.on('call', (value, way, obj) => {
        if (value === 'itemAnimation') {
          if (way === 'enter') {
            this.$gsap.to(obj.el, {
              scaleX: 1,
              ease: 'expo.out',
              duration: 3
            })
          }
        }
      })
    }
  }
}
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@400;500;600;700;800&display=swap');
.font-fam-inter {
  font-family: 'Inter', sans-serif;
}
.font-fam-raleway {
  font-family: 'Raleway', sans-serif;
}
</style>