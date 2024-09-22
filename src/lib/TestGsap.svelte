<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    const races = document.querySelector(".races");

    function getScrollAmount() {
      let racesWidth = races.scrollWidth;
      return -(racesWidth - window.innerWidth);
    }

    const tween = gsap.to(races, {
      x: getScrollAmount,
      duration: 3,
      ease: "none",
    });

    ScrollTrigger.create({
      trigger: ".racesWrapper",
      start: "top 20%",
      end: () => `+=${getScrollAmount() * -1}`,
      pin: true,
      animation: tween,
      scrub: 1,
      invalidateOnRefresh: true,
      markers: true,
    });
  });
</script>

<div class="space-50vh lightBG"></div>

<div class="racesWrapper">
  <div class="races">
    <h2>Monaco</h2>
    <h2>Austria</h2>
    <h2>Hungary</h2>
    <h2>Netherlands</h2>
    <h2>Japan</h2>
  </div>
</div>

<div class="space-100vh lightBG"></div>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Staatliches&display=swap");

  .races {
    width: fit-content;
    display: flex;
    flex-wrap: nowrap;
  }

  .races h2 {
    font-family: "Staatliches", cursive;
    font-size: 30vw;
    flex-shrink: 0;
    padding-right: 0.3em;
    padding-left: 0.3em;
    color: #e10600;

    margin: 0;
  }

  .races h2:last-of-type {
    background: #e1e1ff;
  }

  .lightBG {
    background: #313143;
  }

  .space-50vh {
    height: 50vh;
  }

  .space-100vh {
    height: 100vh;
  }
</style>
