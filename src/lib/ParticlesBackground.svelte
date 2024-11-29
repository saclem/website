<script>
  import { onMount } from 'svelte';
  import Particles from "svelte-particles";
  import { loadFull } from "tsparticles";

  let particlesInit = async (engine) => {
    await loadFull(engine);
  };

  const options = {
    background: {
      opacity: 0
    },
    particles: {
      number: {
        value: 80,
        density: {
          enable: true,
          value_area: 800
        }
      },
      color: {
        value: "#ffffff"
      },
      shape: {
        type: "circle"
      },
      opacity: {
        value: 0.5,
        random: false
      },
      size: {
        value: 3,
        random: true
      },
      links: {
        enable: true,
        distance: 150,
        color: "#ffffff",
        opacity: 0.4,
        width: 1
      },
      move: {
        enable: true,
        speed: 2,
        direction: "none",
        random: false,
        straight: false,
        outModes: "out",
        bounce: false
      }
    },
    interactivity: {
      detectsOn: "canvas",
      events: {
        onHover: {
          enable: true,
          mode: "grab"
        },
        resize: true
      },
      modes: {
        grab: {
          distance: 140,
          links: {
            opacity: 1
          }
        }
      }
    },
    detectRetina: true
  };
</script>

<div class="absolute inset-0 z-0">
  <Particles
    id="tsparticles"
    options={options}
    particlesInit={particlesInit}
  />
</div>