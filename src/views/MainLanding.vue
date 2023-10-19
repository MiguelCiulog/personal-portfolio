<template>
  <div class="flex flex-col gap-[2.5rem]">
    <!-- introduction section -->
    <div class="divCenter">
      <p
        id="text_scroll"
        ref="textScroll"
        class="lg:text-xl text-md acrlyic w-auto text-center selector"
      ></p>
    </div>
    <section class="pt-2">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Professional background
      </h2>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        Experienced Software Engineer and Back-End Developer skilled in crafting
        efficient web solutions with a focus on
        <strong>enhancing developer experience</strong>, with a strong
        foundation in <strong>RESTful API development</strong>,
        <strong>database management</strong>, and simple, yet efficient
        <strong>DevOps practices</strong>.
      </p>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        Hungry for knowledge, collaborative individual and possess analytical
        skills. Enjoys problem solving and willing to adapt to changes in the
        industry to stay on top.
      </p>
    </section>
    <!-- info section -->
    <section class="">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Bio
      </h2>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        With a strong passion for technology, computers and efficiency, I am
        delighted to tinker with multiple <strong>Linux</strong> distributions
        and customizing <strong>VIM</strong>. Outside of programming, I have
        hobbies such as <strong>playing music</strong>,
        <strong>video games</strong>, and
        <strong>customizing mechanical/ergonomic keyboards</strong>.
      </p>
    </section>
    <!-- journey section -->
    <section class="">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Journey
      </h2>
      <br />
      <div class="flex flex-col gap-2">
        <p class="lg:text-lg text-sm text-justify">
          <strong>2018:</strong>
          &nbsp; Joined FIRST Robotics Competition
        </p>
        <p class="lg:text-lg text-sm text-justify">
          <strong>2019:</strong>
          &nbsp; Started studying Software Engineering at Sonora Technological
          Institute
        </p>
        <p class="lg:text-lg text-sm text-justify">
          <strong>2022:</strong>
          &nbsp; Started working at Ludens Productions
        </p>
      </div>
    </section>
    <section class="">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Contact
      </h2>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        Do you wish to connect and discuss one of my projects, explore potential
        opportunities, or simply engage in a casual conversation?
        <br />
        You can email me at: <strong>angel.ciulog7@gmail.com</strong>
        <br />
        You can also find my profile on
        <strong class="underline"
          ><a href="https://github.com/MiguelCiulog">Github</a></strong
        >.
      </p>
    </section>
  </div>
</template>

<script>
import TypeIt from 'typeit';
import 'animate.css';
import { ref } from 'vue';

export default {
	data() {
		return {
			display: false
		};
	},
	setup() {
		const textScroll = ref('');

		if (textScroll.value !== '') {
			textScroll.value === '';
		}
	},
	mounted() {
		new TypeIt('#text_scroll', {
			speed: 50,
			waitUntilVisible: true,
			startDelay: 100,
			startDelete: true,
			// remove cursor when finished
			afterComplete: function (instance) {
				instance.destroy();
			}
		})
			.type('Hello! I am a backend developer based in Mexico.')
			.go();
	}
};
</script>

<style>
  .selector {
    background-color: var(--bg-sel);
  }

  .copyright {
    animation: fadeInLeft;
    /* referring directly to the animation's @keyframe declaration */
    animation-duration: 1s;
    /* don't forget to set a duration! */
    animation-delay: 1s;
  }
</style>
