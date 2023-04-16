<script lang="ts" setup>
interface Card {
  title: string;
  description: string;
  image: string;
  link: string;
  theme: string;
}

const cards: Card[] = [
  {
    title: "Sedans",
    description:
      "Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city or on your next road trip.",
    image: "icon-sedans.svg", // import image from assets/images/icon-sedans.svg
    link: "#",
    theme: "primary",
  },
  {
    title: "SUVs",
    description:
      "Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacation and off-road adventures.",
    image: "icon-suvs.svg", // import image from assets/images/icon-suvs.svg
    link: "#",
    theme: "secondary",
  },
  {
    title: "Luxury",
    description:
      "Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury rental and arrive in style.",
    image: "icon-luxury.svg", // import image from assets/images/icon-luxury.svg
    link: "#",
    theme: "tertiary",
  },
];
</script>

<template>
  <div class="ThreeColumnPreviewCard">
    <div class="ThreeColumnPreviewCard-container">
      <PreviewCard v-for="(card, index) in cards" :key="index" :card="card" />
    </div>
  </div>
</template>
