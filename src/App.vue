<template>
  <header>
    <h3>Mini Blog about Animals</h3>
    <nav>
      <ul>
        <li><a href="#">Horse</a></li>
        <li><a href="#">Tiger</a></li>
        <li><a href="#">Giraffe</a></li>
        <li><a href="#">Elephant</a></li>
        <li><a href="#">Fox</a></li>
        <li>
          <a href="#"
            ><img
              class="searchIcon"
              src="https://i.ibb.co.com/3Y0jFGn/free-icon-search-magnifier-symbol-of-interface-51658.png"
          /></a>
        </li>
      </ul>
    </nav>
  </header>

  <main>
    <div class="blog-posts">
      <ul class="posts">
        <ul class="firstColumn">
          <li class="container">
            <div class="small">
              <img src="./assets/images/spirit.jpeg" />
            </div>
            <div class="bottom-left">Horse</div>
            <div class="bottom-left2">horse horse horse</div>
          </li>
          <li class="container">
            <div class="small">
              <img src="./assets/images/tgr.jpeg" />
            </div>
            <div class="bottom-left">Tiger</div>
            <div class="bottom-left2">tiger tiger tiger</div>
          </li>
        </ul>

        <ul class="secondColumn">
          <li class="container">
            <div class="large">
              <img class="large" src="./assets/images/giraffe.jpeg" />
            </div>
            <div class="travelButton">Travel</div>
            <div class="foodButton">Food</div>
            <div class="bottom-left">Giraffe</div>
            <div class="bottom-left2">giraffe giraffe giraffe</div>
          </li>
        </ul>

        <ul class="thirdColumn">
          <li class="container">
            <div class="small">
              <img src="./assets/images/elephant.jpeg" />
            </div>
            <div class="bottom-left">Elephant</div>
            <div class="bottom-left2">elephant elephant elephant</div>
          </li>
          <li class="container">
            <div class="small">
              <img src="./assets/images/fox.jpeg" />
            </div>
            <div class="bottom-left">Fox</div>
            <div class="bottom-left2">fox fox fox</div>
          </li>
        </ul>
      </ul>
    </div>
  </main>
</template>

<script></script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: rgb(205, 150, 1);
  border-radius: 4px;
  padding: 4px;
}

header ul {
  display: flex;
  align-items: center;
}

.searchIcon {
  width: 16px;
  height: 16px;
  margin-top: 5px;
}

nav li {
  display: inline;
  margin-right: 20px;
}

nav li a {
  color: rgb(255, 255, 255);
}

h3 {
  color: white;
}

nav ul a {
  text-decoration: none;
}

main {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  margin-left: 80px;
  margin-top: 80px;
}

.blog-posts {
  display: flex;
  width: 80%;
}

.posts {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.posts ul {
  padding: 0;
  margin: 0;
  width: 32%;
}

.posts li {
  list-style: none;
  padding: 5px;
  margin: 5px;
}

.container {
  position: relative;
}

.bottom-left {
  position: absolute;
  font-size: 19px;
  font-weight: 300;
  color: white;
  bottom: 40px;
  left: 20px;
  z-index: 2;
}

.bottom-left2 {
  position: absolute;
  font-size: 15px;
  font-weight: 300;
  color: rgb(201, 201, 201);
  bottom: 20px;
  left: 20px;
  z-index: 2;
}

.small {
  width: 100%;
  height: 100%;
  z-index: 1;
  position: relative;
}

.small:after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 30%;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0));
  border-radius: 3px;
  z-index: 2;
}

.large {
  width: 100%;
  height: 100%;
  position: relative;
}

.large:after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 30%;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0));
  border-radius: 3px;
  z-index: 2;
}


.travelButton {
  position: absolute;
  font-size: 14px;
  font-weight: 300;
  color: rgb(201, 201, 201);
  background-color: rgb(255, 22, 22);
  padding: 3px;
  padding-left: 10px;
  padding-right: 10px;
  border-radius: 3px;
  bottom: 80px;
  left: 20px;
}

.foodButton {
  position: absolute;
  font-size: 14px;
  font-weight: 300;
  color: rgb(201, 201, 201);
  background-color: rgb(1, 128, 255);
  padding: 3px;
  padding-left: 10px;
  padding-right: 10px;
  border-radius: 3px;
  bottom: 80px;
  left: 80px;
}

.firstColumn {
  display: flex;
  flex-direction: column;
}

.firstColumn li {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}

.secondColumn {
  display: flex;
  flex-direction: column;
}

.secondColumn li {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}

.thirdColumn {
  display: flex;
  flex-direction: column;
}

.thirdColumn li {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}

.posts ul {
  width: 100%;
  height: 100%;
}

.posts img {
  width: 100%;
  height: 100%;
  border-radius: 3px;
  object-fit: cover;
}
</style>
