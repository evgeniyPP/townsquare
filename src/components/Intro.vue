<template>
  <div class="intro">
    <img src="static/apple-icon.png" alt="" class="logo" />
    <div>
      Добро пожаловать на
      <b>Виртуальную Площадь</b> и в <b>Гримуар</b> для игры Blood on the
      Clocktower! Пожалуйста, добавьте больше игроков через
      <span class="button" @click="toggleMenu">
        <font-awesome-icon icon="cog" /> Меню
      </span>
      в правом верхнем углу или нажатием <b>[A]</b>. Вы также можете
      присоединиться к игровой сессии, нажав <b>[J]</b>.<br />
      <div class="footer">
        Этот проект в открытом доступе и может быть найден на
        <a href="https://github.com/bra1n/townsquare" target="_blank">GitHub</a>
        (<a href="https://github.com/evgeniyPP/townsquare" target="_blank"
          >перевод</a
        >). Он никаким образом не связан с The Pandemonium Institute. "Blood on
        the Clocktower" является торговой маркой Стивена Медвуэй и The
        Pandemonium Institute.
      </div>
    </div>
  </div>
</template>

<script>
import { mapMutations } from "vuex";

export default {
  data() {
    return {};
  },
  methods: mapMutations(["toggleMenu"])
};
</script>

<style scoped lang="scss">
// Intro
.intro {
  text-align: center;
  width: 50%;
  font-size: 120%;
  position: absolute;
  padding: 10px;
  background: rgba(0, 0, 0, 0.5);
  border: 3px solid black;
  border-radius: 10px;
  z-index: 3;
  display: flex;
  justify-content: center;
  a {
    color: white;
  }
  a.redirect {
    display: block;
    text-decoration: none;
    position: absolute;
    top: 100%;
    margin-top: 2vh;
    padding: 10px;
    background: rgba(0, 0, 0, 0.5);
    border: 3px solid black;
    border-radius: 10px;

    &:hover {
      color: red;
    }
    img {
      width: 120px;
      display: block;
      margin: auto;
      margin-bottom: 1vh;
    }
  }

  img.logo {
    position: absolute;
    bottom: 100%;
    width: 25vh;
    margin-bottom: 2vh;
    max-width: 192px;
    border-radius: 50%;
    box-shadow: 0 0 10px black;
    border: 3px solid black;
  }
  .footer {
    font-size: 60%;
    opacity: 0.75;
  }
}
</style>
