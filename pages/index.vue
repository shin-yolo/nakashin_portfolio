<template>
  <div class="page-index">
    <div class="page-container">
      <h2 class="page-title">Nakashin Portfolio</h2>
      <ul class="page-ul">
        <li class="page-li">
          <nuxt-link to="/about">About</nuxt-link>
        </li>
        <li class="page-li">
          <nuxt-link to="/skills">Skills</nuxt-link>
        </li>
        <li class="page-li">
          <nuxt-link to="/works">Works</nuxt-link>
        </li>
        <li class="page-li">
          <nuxt-link to="/contact">Contact</nuxt-link>
        </li>
      </ul>
    </div>
    <div class="page-icon">
      <a
        href="https://twitter.com/shin_yolo1006"
        target="_blank"
        class="fa fa-github"
      ></a>
      <a
        href="https://twitter.com/shin_yolo1006"
        target="_blank"
        class="fa fa-twitter"
      ></a>
      <a
        href="https://www.instagram.com/ns_kny106/?hl=ja"
        target="_blank"
        class="fa fa-instagram"
      ></a>
    </div>
  </div>
</template>

<script>
import "vuetify/dist/vuetify.min.css";
export default {};
</script>

<style lang="scss" scoped>
.page-container {
  background-image: url("~@/assets/img/niku.png");
  background-size: 20%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;

  .page {
    &-title {
      margin-bottom: 50px;
      font-size: 2rem;
      text-align: center;
    }
    &-ul {
      display: flex;
      padding: 0;
      margin: 0;
      list-style: none;
      align-items: center;
      flex-direction: column;
    }

    &-li {
      padding: 0;
      margin-bottom: 20px;
      font-size: 1.5rem;

      & > a {
        color: $color-black;
        text-decoration: none !important;
        text-transform: uppercase;
        position: relative;
        display: inline-block;

        &::after {
          position: absolute;
          bottom: -4px;
          left: 0;
          content: "";
          width: 100%;
          height: 2px;
          background: #333;
          transform: scale(0, 1);
          transform-origin: left top;
          transition: transform 0.3s;
        }
        &:hover::after {
          transform: scale(1, 1);
        }
      }
    }
  }
}

.page-icon {
  position: absolute;
  bottom: 40px;
  left: 50%;
  transform: translateX(-50%);
}
/* Style all font awesome icons */
.fa {
  padding: 10px;
  font-size: 20px;
  width: 40px;
  text-align: center;
  text-decoration: none;
  border-radius: 50%;
  margin-right: 10px;
  &:last-child {
    margin-right: 0;
  }
}

/* Add a hover effect if you want */
.fa:hover {
  opacity: 0.7;
}

/* Set a specific color for each brand */

/* Facebook */
.fa-github {
  background: #430297;
  color: white;
}

/* Twitter */
.fa-twitter {
  background: #55acee;
  color: white;
}
.fa-instagram {
  background: -webkit-linear-gradient(135deg, #427eff 0%, #f13f79 70%) no-repeat;
  background: linear-gradient(135deg, #427eff 0%, #f13f79 70%) no-repeat; /*グラデーション①*/
  color: white;
}

@media screen and (max-width: 600px) {
  .page-container {
    background-image: none;
  }
}
</style>
