<script>
  import { onMount } from "svelte";

  import Section from "./homepage-section.svelte";
  import Bubble from "./bubble.svelte";

  let bubbleSize;

  const technologies = [
    "JavaScript",
    "TypeScript",
    "Rust",
    "Python",
    "React",
    "Svelte",
    "Flutter",
    "Dart",
    "GCP",
    "AWS",
    "Firebase",
    "Vercel",
    "Hasura",
    "PostgreSQL",
    "Firebase",
    "Docker",
    "Kubernetes",
    "Terraform",
  ];
  let technologiesWithPositions = [];

  function getPosition(technology, maxX, maxY) {
    console.log("TESTING");
    let index = technologiesWithPositions.findIndex((value)=>value == technology);

    if (index == -1) {
      let x = Math.random() * maxX;
      let y = Math.random() * maxY;
      if (
        technologiesWithPositions.some(
          (bubble) =>
            Math.sqrt(Math.pow(bubble.x - x, 2) + Math.pow(bubble.y - y, 2)) <
            bubbleSize
        )
      ) {
        return getPosition(technology, maxX, maxY);
      } else {
        return {
          technology: technology,
          x: x,
          y: y,
        };
      }
    }
  }

  onMount(() => {
    console.log("MOUNTT");

    let width = window.innerWidth;
    let height = window.innerHeight;
    let centerX = width / 2;
    let centerY = height / 2;

    console.log(width, height, technologies.length);

    bubbleSize = Math.sqrt((width * height) / (technologies.length * 2)) / 2;
    console.log(bubbleSize);

    technologies.forEach((technology) => {
      technologiesWithPositions.push(getPosition(technology, width, height));
    });
  });
</script>

<style>
</style>

<Section backgroundColor="#ffffff" >
  {#each technologiesWithPositions as technology}
    <Bubble
      name={technology}
      x={technology.x}
      y={technology.y}
      size={bubbleSize} />
  {/each}
</Section>
