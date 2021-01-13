<template>
  <div class="bio-section">
    <div class="bio-section-container">
      <div class="bio-bubble">
        <h1 class="bio-label"/>
        <div class="bio-image"></div>
        <div class="bio-text">
          <p style="padding-left: 18px">
            Graduated from the University of Mary Hardin-Baylor with a <b>Bachelor's of Science in Computer Science, minoring in Mathematics, Summa Cum Laude with a 4.0 GPA.</b>
            I have experience working as a <b>full-stack software engineer developing REST APIs</b> in multiple languages. I am a <b>quick learner</b> and used to <b>learning difficult skills on the fly.</b>
            Through my work experience, I also have learned how to <b>communicate</b> technical requirements to non-technical cohorts <b>effectively and efficiently.</b>
            My goals are to broaden my experience and and use my <b>passion for software development</b> to sharpen my abilities.
          </p>
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

@media (min-width: 1140px) {
  .bio-bubble {
    width: 65%;
    padding: 10px;
    margin: auto;
    height: 18rem;
    background-color: var(--js-white);
    margin-top: 7rem;
    border-radius: 5px;
    animation: on-awake 1s ease-out 1;
    justify-content: space-around;
    display: flex;
    flex-direction: row;
    box-shadow: 10px 10px 8px rgba(0, 0, 0, 0.5);
  }

  .bio-text {
    border-left: solid 2px var(--js-primary);
    max-width: 70%;
    margin-left: 0;
  }

  .bio-image {
    background-image: url('/assets/profile.jpg');
    background-repeat: no-repeat;
    border-radius: 50%;
    min-width: 160px;
    min-height: 160px;
  }
}

@media (max-width: 1139px) {
  .bio-bubble {
    width: 90%;
    padding: 10px;
    margin: auto;
    height: 15rem;
    background-color: var(--js-white);
    margin-top: 8rem;
    border-radius: 5px;
    animation: on-awake 1s ease-out 1;
    justify-content: space-around;
    display: flex;
    flex-direction: row;
    box-shadow: 10px 10px 8px rgba(0, 0, 0, 0.5);
  }

  .bio-text {
  }

  .bio-image {
    padding: 0px;
    margin: 0px;
    width: 0px;
    height: 0px;
  }

  .bio-label {
    font-size: 24px;
    left: 10%;
    margin-top: 0px;
    position: absolute;
  }

  .bio-label::before {
    content: "About me";
  }
}

.bio-bubble > div {
  margin: auto;
}

@keyframes on-awake {
  0% { opacity: 0; transform: scale(0.95) translateY(100px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
</style>
