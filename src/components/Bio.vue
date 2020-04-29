<template>
  <div class="bio-section">
    <div class="bio-section-container">
      <div class="bio-bubble">
        <div class="bio-image"></div>
        <div class="bio-text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris dapibus consequat libero et tempor. Sed eget laoreet risus, at consectetur ligula. Nunc magna ante, tincidunt vitae suscipit congue
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bio-section {
  height: 32rem;
  width: 100%;
  clip-path: polygon(0 17%, 100% 2%, 100% 100%, 0 100%)
}

.bio-section-container {
  width: 100%;
  height: 30rem;
  background-color: var(--js-primary-soft);
  border-radius: 2px;
  position: absolute;
  box-shadow: inset 4px 90px 30px rgba(0,0,0,0.2);
}

.bio-bubble {
  width: 60%;
  padding: 10px;
  margin: auto;
  height: 16rem;
  background-color: var(--js-white);
  margin-top: 9rem;
  border-radius: 5px;
  animation: on-awake 1s ease-out 1;
  justify-content: space-around;
  display: flex;
  flex-direction: row;
  box-shadow: 10px 10px 8px rgba(0, 0, 0, 0.5);
}

.bio-bubble > div {
  padding: 18px;
  margin: auto;
}

.bio-text {
  border-left: solid 2px var(--js-primary);
  max-width: 70%;
}

.bio-image {
  background-image: url('/assets/profile.jpg');
  background-repeat: no-repeat;
  border-radius: 50%;
  min-width: 160px;
  min-height: 160px;
}

@keyframes on-awake {
  0% { opacity: 0; transform: scale(0.95) translateY(100px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
</style>
