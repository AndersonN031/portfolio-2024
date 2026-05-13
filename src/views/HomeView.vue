<template>
  <main
    class="mt-10 md:mt-1 flex flex-col-reverse gap-8 items-center md:flex-row md:gap-16 md:justify-center min-h-[65vh] md:min-h-[80vh]"
  >
    <div class="space-y-3 text-center md:text-left px-10">
      <p class="text-amber-200 text-sm tracking-widest uppercase">
        Olá mundo, eu sou
      </p>
      <h1 class="text-4xl font-bold md:text-5xl text-white fadein-up">
        Anderson Nunes
      </h1>
      <div class="py-1">
        <h1
          class="typewrite text-xl font-semibold text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-yellow-500 md:text-2xl fadein-up"
          ref="typewriter"
        >
          <span class="wrap">{{ txt }}</span>
        </h1>
      </div>
      <p class="text-[#c1c1c1] pr-4 fade-in-from-left text-sm md:text-base">
        Bem-vindo(a) ao meu site pessoal. <span class="wave">👋🏼</span>
      </p>

      <!-- Botões CTA -->
      <div
        class="flex gap-3 justify-center md:justify-start pt-2 fade-in-from-left"
      >
        <a
          href="/portfolio"
          class="px-5 py-2 bg-amber-400 text-black font-semibold rounded-lg text-sm hover:bg-amber-300 transition-all duration-200 hover:scale-105"
        >
          Ver Projetos
        </a>
        <a
          href="/cv-anderson-nunes.pdf"
          download="Anderson_Nunes_CV.pdf"
          class="px-5 py-2 border border-amber-400 text-amber-200 font-semibold rounded-lg text-sm hover:bg-amber-400 hover:bg-opacity-10 transition-all duration-200 hover:scale-105"
        >
          Baixar Currículo
        </a>
      </div>

      <!-- Bloco de conquistas -->
      <div
        class="flex gap-6 justify-center md:justify-start pt-4 fade-in-from-left"
      >
        <div class="text-center md:text-left">
          <div class="text-2xl font-bold text-amber-300">2+</div>
          <div class="text-xs text-[#888] leading-tight">
            Anos de<br />experiência
          </div>
        </div>
        <div class="w-px bg-[#383838]"></div>
        <div class="text-center md:text-left">
          <div class="text-2xl font-bold text-amber-300">2</div>
          <div class="text-xs text-[#888] leading-tight">
            Empresas<br />atuadas
          </div>
        </div>
        <div class="w-px bg-[#383838]"></div>
        <div class="text-center md:text-left">
          <div class="text-2xl font-bold text-amber-300">6+</div>
          <div class="text-xs text-[#888] leading-tight">
            Projetos<br />entregues
          </div>
        </div>
      </div>
    </div>

    <div class="flex justify-center md:justify-start fadein-right">
      <img
        alt="avatar"
        width="300"
        height="300"
        src="../images/ANDERSON_08.jpg"
        class="rounded-image pict"
      />
    </div>
  </main>
</template>

<style>
.rounded-image {
  border-radius: 50%;
  width: 320px;
  height: 320px;
  object-fit: cover;
}
</style>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      toRotate: [
        "Desenvolvedor Full-Stack",
        "Node.js · NestJS · React",
        "TypeScript · PostgreSQL · Docker",
      ],
      period: 2500,
      txt: "",
      loopNum: 0,
      isDeleting: false,
    };
  },
  mounted() {
    this.$nextTick(() => {
      this.tick();
    });
  },
  methods: {
    tick() {
      let typewriter = this.$refs.typewriter;
      if (!typewriter) return;

      let i = this.loopNum % this.toRotate.length;
      let fullTxt = this.toRotate[i];

      this.txt = this.isDeleting
        ? fullTxt.substring(0, this.txt.length - 1)
        : fullTxt.substring(0, this.txt.length + 1);
      typewriter.innerHTML = `<span class="wrap">${this.txt}</span>`;

      let that = this;
      let delta = 200 - Math.random() * 100;
      if (this.isDeleting) delta /= 2;

      if (!this.isDeleting && this.txt === fullTxt) {
        delta = this.period;
        this.isDeleting = true;
      } else if (this.isDeleting && this.txt === "") {
        this.isDeleting = false;
        this.loopNum++;
        delta = 500;
      }

      setTimeout(() => {
        that.tick();
      }, delta);
    },
  },
};
</script>

<style>
body {
  overflow-y: scroll;
  overflow-x: hidden;
}

.typewrite > .wrap {
  border-right: 0.08em solid #fff;
}

.wave {
  animation-name: wave-animation;
  animation-duration: 2.5s;
  animation-iteration-count: infinite;
  transform-origin: 70% 70%;
  display: inline-block;
}

@keyframes wave-animation {
  0% {
    transform: rotate(0deg);
  }
  10% {
    transform: rotate(14deg);
  }
  20% {
    transform: rotate(-8deg);
  }
  30% {
    transform: rotate(14deg);
  }
  40% {
    transform: rotate(-4deg);
  }
  50% {
    transform: rotate(10deg);
  }
  60% {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(0deg);
  }
}

.pict {
  box-shadow: 0px 0px 73px -9px rgba(255, 219, 112, 0.44);
  -webkit-box-shadow: 0px 0px 73px -9px rgba(255, 219, 112, 0.44);
  -moz-box-shadow: 0px 0px 73px -9px rgba(255, 219, 112, 0.44);
}

.fadein-up {
  opacity: 0;
  animation-name: fadeInUp;
  animation-duration: 0.5s;
  animation-fill-mode: forwards;
  animation-delay: 500ms;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate3d(0, 100%, 0);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}

.fade-in-from-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
  animation-delay: 700ms;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-60px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadein-right {
  opacity: 0;
  animation: fadeInRight 0.5s ease-out forwards;
  animation-delay: 500ms;
}

@keyframes fadeInRight {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadein-bot {
  opacity: 0;
  animation: fadeInBot 0.5s forwards;
}

@keyframes fadeInBot {
  from {
    opacity: 0;
    transform: translate3d(0, -100%, 0);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}
</style>
