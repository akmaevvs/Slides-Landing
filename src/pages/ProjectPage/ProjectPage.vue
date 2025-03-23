<template>
  <div class="wrapper">
    <div class="wrapper-content">
      <div class="project-subtitle">Projects</div>
      <img class="project-img" :src="New" alt="new" />
    </div>
    <div class="project-title">
      Create and edit pages online.<br />
      Export as finished, <span class="highlight">ready-to-upload</span> <br />
      project.
    </div>
    <div class="project-description">
      The Projects are here! Keep and maintain multiple pages in separate projects. <br />` Edit the
      content, upload media, add meta-tags and much more...
    </div>
    <button class="project-button">Start New Project →</button>

    <img :src="Page" alt="new" />
  </div>
</template>
<script setup lang="ts">
import New from '@/app/assets/images/new.svg';
import Page from '@/app/assets/images/Page.svg';
</script>

<style lang="scss">
.wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #1a1a2e;
  color: white;
  text-align: center;
  gap: 20px;

  .wrapper-content {
    position: relative;
    margin-top: 120px;
  }

  .project-img {
    position: absolute;
    top: -15px;
    right: -45px;
  }
}

.project-subtitle {
  font-size: 18px;
  color: #b0b0b0;
}

.project-title {
  font-size: 45px;
  font-weight: bold;

  .highlight {
    color: #805ad5;
  }
}

.project-description {
  color: #b0b0b0;
  max-width: 600px;
}

.project-button {
  margin-top: 12px;
  padding: 12px 24px;
  background-color: #805ad5;
  color: white;
  border: none;
  border-radius: 8px;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.3s;
  margin-bottom: 55px;
}

.project-button:hover {
  background-color: #6a48c3;
}
</style>
