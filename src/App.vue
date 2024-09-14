<template>
  <div class="app-container">
    <header class="header">
      <h1>Mini Blog about Animals</h1>
      <nav class="nav">
        <a href="#">Horse</a>
        <a href="#">Tiger</a>
        <a href="#">Giraffe</a>
        <a href="#">Elephant</a>
        <a href="#">Fox</a>
      </nav>
    </header>

    <section class="blog-section">
      <div
        class="blog-card"
        v-for="(blog, index) in blogs"
        :key="index"
        :class="{ 'blog-card-large': index === 2 }"
      >
        <img :src="blog.image" class="blog-image" />
        <div class="blog-content">
          <h3>{{ blog.title }}</h3>
          <p>{{ blog.date }}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import horseImage from "@/assets/images/spirit.jpeg";
import tigerImage from "@/assets/images/tgr.jpeg";
import giraffeImage from "@/assets/images/giraffe.jpeg";
import elephantImage from "@/assets/images/elephant.jpeg";
import foxImage from "@/assets/images/fox.jpeg";

export default {
  data() {
    return {
      blogs: [
        {
          image: horseImage,
          title: "Horse",
          date: "July 2, 2018",
        },
        {
          image: tigerImage,
          title: "Tiger",
          date: "March 19, 2019",
        },
        {
          image: giraffeImage,
          title: "Giraffe",
          date: "April 25, 2010",
        },
        {
          image: elephantImage,
          title: "Elephant",
          date: "September 13, 2003",
        },
        {
          image: foxImage,
          title: "Fox",
          date: "December 29, 2021",
        },
      ],
    };
  },
};
</script>

<style scoped>
.app-container {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

.header {
  background-color: #f9f9f9;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #ddd;
}

.header h1 {
  font-size: 28px;
}

.nav a {
  margin: 0 15px;
  text-decoration: none;
  color: #555;
}

.nav a:hover {
  color: #000;
}

.blog-section {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  padding: 20px;
}

.blog-card {
  background-color: #f9f9f9;
  border-radius: 10px;
  overflow: hidden;
  transition: 0.3s;
  position: relative;
}

.blog-card:hover {
  transform: scale(1.05);
}

.blog-card-large {
  grid-row: span 2;
}

.blog-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.blog-content {
  position: absolute;
  bottom: 0;
  width: 100%;
  padding: 15px;
  background: rgba(0, 0, 0, 0.5);
  color: #fff;
  text-align: center;
}

h3 {
  margin: 5px 0;
  font-size: 18px;
}

p {
  font-size: 14px;
}
</style>
