<template lang="pug">
  .nintendo-ds#css
    .top-screen
      .speaker-hole#sh1
      .speaker-hole#sh2
      .screen
      .speaker-hole#sh3
      .speaker-hole#sh4
    .hinge
      .mic
      .light
    .bottom-screen
      .screen
      .d-pad
        .d-pad-marker#dpm1
        .d-pad-marker#dpm2
        .d-pad-marker#dpm3
        .d-pad-marker#dpm4
      .button#X X
      .button#A A
      .button#B B
      .button#Y Y
      .small-button#start
      .small-button#select
</template>

<style>
:root {
  --pink: #f6c5ce;
  --shadow: #eba4b2;
  --black: #270b0c;
}
</style>
<style scoped>
.nintendo-ds {
  width: 414px;
  height: 431px;
  /* make the DS a fixed background centered in viewport */
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) scale(2);
  transform-origin: center;
  z-index: -1; /* behind other content */
  pointer-events: none; /* allow clicking through */
  font-family: "Open Sans", sans-serif;
}

.top-screen {
  position: absolute;
  width: 100%;
  height: 46.5%;
  /* border: 1px solid red; */
  border-radius: 15px 15px 5px 5px;
  background: var(--pink);
  box-shadow:
    inset 10px 10px 12px -2px var(--shadow),
    inset -2px 5px 3px 1px var(--shadow),
    inset -5px 5px 5px 2px white,
    0px -1px 2px 2px #b58688;
}

.screen {
  position: absolute;
  width: 51.5%;
  /* border: 1px solid blue; */
  height: 83.5%;
  border-radius: 3px;
  top: 9.5%;
  left: 24%;
  box-shadow: 0px 0px 3px 0px #875f68;
}

.screen::after {
  position: absolute;
  content: "";
  width: 91%;
  height: 87%;
  /* border: 1px solid grey; */
  box-shadow: 0px 0px 1px 2px rgba(0, 0, 0, 0.5);
  left: 4%;
  top: 6%;
  background: rgb(73, 73, 73);
  background: linear-gradient(
    323deg,
    rgba(73, 73, 73, 1) 42%,
    rgba(245, 243, 245, 1) 85%
  );
}

.speaker-hole {
  position: absolute;
  width: 5px;
  height: 5px;
  background: var(--black);
  border-radius: 2.5px;
}

.speaker-hole::after {
  position: absolute;
  content: "";
  height: 5px;
  width: 5px;
  border-radius: 2.5px;
  background: var(--black);
  left: 16px;
}

.speaker-hole::before {
  position: absolute;
  content: "";
  height: 5px;
  width: 5px;
  border-radius: 2.5px;
  background: var(--black);
  left: 31px;
}

#sh1 {
  left: 30px;
  top: 94px;
}

#sh2 {
  left: 30px;
  top: 110px;
}

#sh3 {
  left: 346px;
  top: 95px;
}

#sh4 {
  left: 346px;
  top: 110px;
}

.hinge {
  position: absolute;
  width: 99.5%;
  top: 46.5%;
  height: 28px;
  border-radius: 25px;
  z-index: 3;
  background: rgb(227, 167, 178);
  background: linear-gradient(
    0deg,
    rgba(176, 121, 132) 0%,
    rgba(227, 167, 178, 1) 10%,
    rgba(251, 205, 213, 1) 65%,
    rgba(227, 167, 178, 1) 100%
  );
  box-shadow: 0px 5px 10px -1px #c67b8e;
}

.hinge::after {
  position: absolute;
  content: "";
  width: 2px;
  height: 100%;
  background: #c99198;
  left: 49px;
}

.hinge::before {
  position: absolute;
  content: "";
  width: 2px;
  height: 100%;
  background: #c99198;
  left: 364px;
}

.mic {
  position: absolute;
  width: 4px;
  height: 10px;
  border-radius: 2px;
  background: var(--black);
  left: 49.5%;
  top: 8px;
}

.light {
  position: absolute;
  height: 67%;
  width: 4px;
  top: 12%;
  border-radius: 10px;
  right: 25px;
  background: rgb(106, 87, 82);
  background: linear-gradient(
    0deg,
    rgba(106, 87, 82, 1) 0%,
    rgba(205, 186, 186, 1) 65%,
    rgba(106, 87, 82, 1) 100%
  );
}

.light::after {
  content: "";
  position: absolute;
  height: 100%;
  width: 4px;
  top: 0;
  border-radius: 10px;
  left: 8px;
  background: rgb(92, 107, 73);
  background: linear-gradient(
    0deg,
    rgba(92, 107, 73, 1) 0%,
    rgba(211, 212, 183, 1) 65%,
    rgba(123, 142, 98, 1) 100%
  );
}

.bottom-screen {
  position: absolute;
  width: 99.5%;
  height: 50%;
  /* border: 1px solid purple; */
  bottom: 0;
  border-radius: 3px 3px 14px 14px;
  background: var(--pink);
  box-shadow: 0px 1px 2px 2px #b58688;
}

.bottom-screen .screen {
  /* border: 1px solid red; */
  top: 24px;
  height: 168px;
  width: 52%;
  background: var(--pink);
  z-index: 1;
}

.bottom-screen .screen::after {
  background: rgb(73, 73, 73);
  background: linear-gradient(
    140deg,
    rgba(73, 73, 73, 1) 42%,
    rgba(245, 243, 245, 1) 85%
  );
}

.bottom-screen .screen::before {
  content: "";
  position: absolute;
  width: 102%;
  height: 109%;
  /* border: 1px solid red; */
  left: -1%;
  top: -7%;
  /* background: #D5929F; */
  z-index: -1;
  border-radius: 5px;
  box-shadow:
    10px 7px 10px 3px #e09aa9,
    -6px 4px 5px 2px var(--pink),
    -12px 4px 8px 3px #fbeaee;
}

.d-pad {
  position: absolute;
  width: 18px;
  height: 54px;
  background: var(--pink);
  border-radius: 3px;
  left: 34px;
  top: 61px;
  border: 2px solid #967178;
}

.d-pad::before {
  position: absolute;
  content: "";
  width: 18px;
  height: 54px;
  background: var(--pink);
  border-radius: 3px;
  border: 2px solid #967178;
  transform: rotate(90deg);
  top: -2px;
  left: -2px;
}

.d-pad::after {
  position: absolute;
  content: "";
  width: 18px;
  height: 54px;
  background: var(--pink);
  border-radius: 3px;
  /* border: 2px solid; */
  top: 0px;
  left: 0px;
}

.d-pad-marker {
  position: absolute;
  width: 2px;
  height: 11px;
  background: #ffe3e4;
  /*   #F4D7D8 */
  z-index: 5;
}

#dpm1 {
  left: 8px;
  top: 6px;
}

#dpm2 {
  left: 8px;
  top: 38px;
}

#dpm3 {
  left: 25px;
  top: 22px;
  transform: rotate(90deg);
}

#dpm4 {
  left: -8px;
  top: 22px;
  transform: rotate(90deg);
}

.button {
  position: absolute;
  width: 21px;
  height: 18px;
  padding-top: 3px;
  border: 1px solid var(--shadow);
  border-radius: 50%;
  z-index: 5;
  font-size: 0.7rem;
  font-weight: 400;
  background: #f3c9cf;
  color: #fff7f9;
  box-shadow:
    3px 2px 3px -2px #bf8691,
    inset 2px 2px 3px -1px #fde7ee;
}

#X {
  right: 35px;
  top: 45px;
}

#A {
  right: 12px;
  top: 69px;
}

#Y {
  right: 59px;
  top: 69px;
}

#B {
  right: 35px;
  top: 92px;
}

.small-button {
  position: absolute;
  width: 11px;
  height: 11px;
  border: 1px solid #bd8993;
  border-radius: 50%;
  bottom: 53px;
  right: 70px;
  box-shadow: 2px 2px 3px -2px #bf8691;
}

#select {
  bottom: 29px;
  right: 70px;
}

#start::after {
  position: absolute;
  content: "START";
  font-size: 7px;
  color: #fff7f9;
  left: 15px;
  top: 2px;
}

#select::after {
  position: absolute;
  content: "SELECT";
  font-size: 7px;
  color: #fff7f9;
  left: 15px;
  top: 2px;
}

button {
  position: absolute;
  top: 6%;
  padding: 6px 15px;
  background: #93e8f5;
  border: none;
  border-radius: 15px;
  font-size: 1.05rem;
  cursor: pointer;
}

.hide {
  display: none;
}

.pink {
  background: var(--pink);
}
</style>
