<template>
    <div class="interesting-links p-3 bg-light border rounded">
      <h3 class="mb-3">{{ title }}</h3>
      <ul class="list-group">
        <li
          v-for="(link, index) in links"
          :key="index"
          class="list-group-item d-flex justify-content-between align-items-center"
        >
          <a :href="link.url" target="_blank" class="link-primary">{{ link.label }}</a>
          <i class="bi bi-box-arrow-up-right"></i>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: "InterestingLinks",
    props: {
      title: {
        type: String,
        default: "ลิงก์น่าสนใจ",
      },
      links: {
        type: Array,
        default: () => [
          { label: "Google", url: "https://www.google.com" },
          { label: "Facebook", url: "https://www.facebook.com" },
          { label: "YouTube", url: "https://www.youtube.com" },
        ],
      },
    },
  };
  </script>
  
  <style scoped>
  .interesting-links a {
    text-decoration: none;
  }
  .interesting-links a:hover {
    text-decoration: underline;
  }
  </style>
  