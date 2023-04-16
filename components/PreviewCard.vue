<script lang="ts" setup>
defineProps<{
  card: {
    title: string;
    description: string;
    image: string;
    link: string;
    theme: string;
  };
}>();
</script>

<template>
  <div
    :class="{
      'ThreeColumnPreviewCard-primary': card.theme === 'primary',
      'ThreeColumnPreviewCard-secondary': card.theme === 'secondary',
      'ThreeColumnPreviewCard-tertiary': card.theme === 'tertiary',
    }"
    class="ThreeColumnPreviewCard-card"
    :key="card.title"
  >
    <div class="ThreeColumnPreviewCard-image">
      <img :src="'/images/' + card.image" :alt="card.title" />
    </div>
    <div class="ThreeColumnPreviewCard-content">
      <h3 class="ThreeColumnPreviewCard-title">{{ card.title }}</h3>
      <p class="ThreeColumnPreviewCard-description">
        {{ card.description }}
      </p>
      <div class="ThreeColumnPreviewCard-linkContainer">
        <NuxtLink
          :class="{
            'is-text-primary': card.theme === 'primary',
            'is-text-secondary': card.theme === 'secondary',
            'is-text-tertiary': card.theme === 'tertiary',
          }"
          class="ThreeColumnPreviewCard-link"
          :to="card.link"
        >
          Learn More
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
