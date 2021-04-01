<template>
  <div id="app">
    <Timer/>
    <div class="timer__aurora"></div>
  </div>
</template>

<script>
import Timer from "./components/Timer";

export default {
  name: "App",

  components: {
    Timer
  }
};
</script>

<style>
body {
  background-color: #fff;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.timer__aurora {
  position: absolute;
  left: -50%;
  top: -50%;
  width: 200vw;
  height: 200vh;
  animation-name: northern;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  background: linear-gradient(10deg, #a1d9b4 20%, #32988a 40%, #000e3c 70%);
}

@keyframes northern {
  0% {
    transform: translate(5%, -2%);
  }
  25% {
    transform: translate(10%, 7%);
  }
  40% {
    transform: rotate(-10deg);
  }
  60% {
    transform: translate(7%, -2%);
  }
  85% {
    transform: translate(6%, 3%) rotate(12deg);
  }
  100% {
    transform: none;
  }
}

</style>
