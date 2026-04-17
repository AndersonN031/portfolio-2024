<script>
export default {
  data() {
    return {
      activeTab: 1,
      frontend: [
        {
          id: 1,
          name: "HTML",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/1051/1051277.png",
          status: "Marcação",
        },
        {
          id: 2,
          name: "CSS",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/732/732190.png",
          status: "Cascading Style",
        },
        {
          id: 3,
          name: "Javascript",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-plain.svg",
          status: "Programação",
        },
        {
          id: 4,
          name: "Typescript",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-plain.svg",
          status: "Programação",
        },
        {
          id: 5,
          name: "ReactJS",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg",
          status: "Biblioteca",
        },
        {
          id: 6,
          name: "NextJS",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-plain.svg",
          status: "Framework",
        },
        {
          id: 7,
          name: "VueJS",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuejs/vuejs-original.svg",
          status: "Framework",
        },
        {
          id: 8,
          name: "Tailwind",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original.svg",
          status: "CSS Framework",
        },
        {
          id: 9,
          name: "Bootstrap",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/bootstrap/bootstrap-original.svg",
          status: "Framework",
        },
      ],
      backend: [
        {
          id: 1,
          name: "NodeJS",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg",
          status: "V8 Engine",
        },
        {
          id: 2,
          name: "NestJS",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nestjs/nestjs-original.svg",
          status: "Framework",
        },
        {
          id: 3,
          name: "PostgreSQL",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg",
          status: "Banco de dados",
        },
        {
          id: 4,
          name: "MongoDB",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mongodb/mongodb-original.svg",
          status: "Banco de dados",
        },
        {
          id: 5,
          name: "Prisma",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/prisma/prisma-original.svg",
          status: "ORM",
        },
        {
          id: 6,
          name: "Redis",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/redis/redis-original.svg",
          status: "Cache & Storage",
        },
        {
          id: 7,
          name: "Socket.IO",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/socketio/socketio-original.svg",
          status: "Real-time",
        },
        {
          id: 8,
          name: "Express",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/express/express-original.svg",
          status: "Framework",
        },
      ],
      tools: [
        {
          id: 1,
          name: "Docker",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original.svg",
          status: "Containers",
        },
        {
          id: 2,
          name: "Git",
          imageUrl:
            "https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png",
          status: "Controle de versão",
        },
        {
          id: 3,
          name: "GitHub",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/25/25231.png",
          status: "Git Hosting",
        },
        {
          id: 4,
          name: "VSCode",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg",
          status: "IDE",
        },
        {
          id: 5,
          name: "Postman",
          imageUrl:
            "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postman/postman-plain.svg",
          status: "API Client",
        },
        {
          id: 6,
          name: "NPM",
          imageUrl:
            "https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png",
          status: "Ger. de pacotes",
        },
      ],
    };
  },
};
</script>

<template>
  <div
    class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5"
  >
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center"
        >
          Sobre mim &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96"></div>
        </div>
      </header>

      <section
        class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center"
      >
        <div class="flex justify-center">
          <img
            alt="avatar"
            width="300"
            height="300"
            src="../images/ANDERSON_08.jpg"
            class="rounded-image"
          />
        </div>
        <div class="md:w-7/12">
          <p
            class="mb-4 fadein-left fadeins-1 text-[#c1c1c1] text-sm md:text-base leading-relaxed"
          >
            Desenvolvedor Full-Stack com foco no Back-End, com experiência em projetos de alto volume
            de dados e regras de negócio complexas. Trabalhei na
            <span class="text-amber-200 font-medium">Bear Systems</span>,
            atuando no core de uma plataforma de delivery com sistema de
            carrinho em tempo real via WebSocket e Redis, autenticação JWT +
            Twilio e arquitetura hexagonal com NestJS e PostgreSQL. Antes, na
            <span class="text-amber-200 font-medium">Bluelogic Sistemas</span>,
            corrigi fluxos críticos de requisição de materiais em NestJS e
            MongoDB.
          </p>
          <p
            class="fadein-left fadeins-2 text-[#c1c1c1] text-sm md:text-base leading-relaxed"
          >
            Tenho domínio de TypeScript/JavaScript, APIs RESTful, bancos
            relacionais (PostgreSQL) e NoSQL (MongoDB), com foco em baixo
            acoplamento, testabilidade e boas práticas de código. Familiaridade
            com Docker. Perfil colaborativo, com boa comunicação e disposição
            para propor melhorias técnicas.
          </p>

          <!-- Badges de experiência -->
          <div class="flex flex-wrap gap-2 mt-5">
            <span
              v-for="badge in [
                'Node.js',
                'NestJS',
                'React',
                'Next.js',
                'TypeScript',
                'PostgreSQL',
                'MongoDB',
                'Docker',
                'Redis',
                'WebSocket',
              ]"
              :key="badge"
              class="px-3 py-1 text-xs rounded-full border border-amber-200 border-opacity-40 text-amber-200 bg-amber-200 bg-opacity-5"
            >
              {{ badge }}
            </span>
          </div>
        </div>
      </section>

      <!-- Experiência profissional -->
      <div class="mt-10">
        <div class="text-xl font-bold text-white mb-5 flex items-center">
          <div class="h-[1px] w-10 bg-amber-200 md:w-20"></div>
          &nbsp; Experiência Profissional
        </div>
        <div class="flex flex-col gap-4">
          <div
            class="border border-[#383838] rounded-xl p-5 hover:border-amber-200 hover:border-opacity-30 transition-all"
          >
            <div class="flex justify-between items-start flex-wrap gap-2 mb-2">
              <div>
                <h3 class="text-white font-semibold text-base">
                  Desenvolvedor Full-Stack
                </h3>
                <span class="text-amber-200 text-sm">Bear Systems</span>
              </div>
              <span
                class="text-xs text-[#888] border border-[#383838] px-3 py-1 rounded-full"
                >2025 – 2026 · Remoto</span
              >
            </div>
            <ul class="text-[#c1c1c1] text-sm space-y-1 mt-3 list-none">
              <li class="flex gap-2">
                <span class="text-amber-400">▸</span> Foco principal em Back-End, desenvolvendo APIs, regras de negócio e integrações
              </li>
              <li class="flex gap-2">
                <span class="text-amber-400">▸</span> Core de plataforma de
                delivery: pedidos, produtos, categorias e empresas com
                Arquitetura Hexagonal
              </li>
              <li class="flex gap-2">
                <span class="text-amber-400">▸</span> Sistema de carrinho em
                tempo real com WebSocket (Socket.IO) e Redis para cache e
                sincronização
              </li>
              <li class="flex gap-2">
                <span class="text-amber-400">▸</span> Autenticação completa com
                JWT e Twilio (validação via SMS)
              </li>
              <li class="flex gap-2">
                <span class="text-amber-400">▸</span> Frontend com Next.js
                (SSR), Zustand, Zod, Shadcn UI e Radix UI
              </li>
            </ul>
            <div class="flex flex-wrap gap-2 mt-3">
              <span
                v-for="t in [
                  'NestJS',
                  'TypeScript',
                  'Prisma',
                  'PostgreSQL',
                  'Docker',
                  'Redis',
                  'WebSocket',
                  'Next.js',
                ]"
                :key="t"
                class="px-2 py-0.5 text-xs rounded bg-[#2a2a2b] text-[#aaa]"
                >{{ t }}</span
              >
            </div>
          </div>

          <div
            class="border border-[#383838] rounded-xl p-5 hover:border-amber-200 hover:border-opacity-30 transition-all"
          >
            <div class="flex justify-between items-start flex-wrap gap-2 mb-2">
              <div>
                <h3 class="text-white font-semibold text-base">
                  Desenvolvedor Full-Stack
                </h3>
                <span class="text-amber-200 text-sm">Bluelogic Sistemas</span>
              </div>
              <span
                class="text-xs text-[#888] border border-[#383838] px-3 py-1 rounded-full"
                >2024 – 2025 · Remoto</span
              >
            </div>
            <ul class="text-[#c1c1c1] text-sm space-y-1 mt-3 list-none">
              <li class="flex gap-2">
                <span class="text-amber-400">▸</span> Correção de bugs em fluxos
                de requisição de materiais em arquitetura MVC com NestJS e
                MongoDB
              </li>
              <li class="flex gap-2">
                <span class="text-amber-400">▸</span> Interfaces de
                gerenciamento de materiais com React.js e TypeScript
              </li>
              <li class="flex gap-2">
                <span class="text-amber-400">▸</span> Contribuições que
                reduziram falhas operacionais e otimizaram a gestão de recursos
              </li>
            </ul>
            <div class="flex flex-wrap gap-2 mt-3">
              <span
                v-for="t in ['NestJS', 'React.js', 'TypeScript', 'MongoDB']"
                :key="t"
                class="px-2 py-0.5 text-xs rounded bg-[#2a2a2b] text-[#aaa]"
                >{{ t }}</span
              >
            </div>
          </div>
        </div>
      </div>
    </article>
  </div>

  <!-- Habilidades -->
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article>
      <header>
        <div class="text-2xl font-bold text-white mb-5 flex items-center">
          <div class="h-[1px] w-10 bg-amber-200 md:w-20"></div>
          &nbsp; Habilidades
        </div>
      </header>

      <section>
        <div>
          <ul
            class="flex flex-wrap text-sm font-medium text-center text-gray-500 mb-5"
          >
            <li class="mr-2">
              <button
                class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{
                  'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 1,
                }"
                @click="activeTab = 1"
              >
                Front-End
              </button>
            </li>
            <li class="mr-2">
              <button
                class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{
                  'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 2,
                }"
                @click="activeTab = 2"
              >
                Back-End
              </button>
            </li>
            <li class="mr-2">
              <button
                class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{
                  'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 3,
                }"
                @click="activeTab = 3"
              >
                Ferramentas
              </button>
            </li>
          </ul>
        </div>

        <div v-show="activeTab === 1">
          <div
            class="grid grid-cols-2 gap-5 pb-16 md:grid-cols-3 xl:grid-cols-4"
          >
            <div v-for="item in frontend" :key="item.id">
              <div
                class="item-tech flex items-center gap-2 border border-amber-200 p-2 hover:bg-amber-200 hover:bg-opacity-10"
              >
                <div
                  class="h-12 w-12 flex items-center justify-center p-0 lg:h-16 lg:w-16"
                >
                  <img
                    :src="item.imageUrl"
                    class="h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                  />
                </div>
                <div class="text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium">{{ item.name }}</div>
                  <div class="text-xs text-gray-400">{{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div v-show="activeTab === 2">
          <div
            class="grid grid-cols-2 gap-4 pb-16 md:grid-cols-3 xl:grid-cols-4"
          >
            <div v-for="item in backend" :key="item.id">
              <div
                class="item-tech flex items-center gap-2 border border-amber-200 p-2 hover:bg-amber-200 hover:bg-opacity-10"
              >
                <div
                  class="h-12 w-12 flex items-center justify-center p-0 lg:h-16 lg:w-16"
                >
                  <img
                    :src="item.imageUrl"
                    class="h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                  />
                </div>
                <div class="text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium">{{ item.name }}</div>
                  <div class="text-xs text-gray-400">{{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div v-show="activeTab === 3">
          <div
            class="grid grid-cols-2 gap-4 pb-16 md:grid-cols-3 xl:grid-cols-4"
          >
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex items-center gap-2 border border-amber-200 p-2 hover:bg-amber-200 hover:bg-opacity-10"
              >
                <div
                  class="h-12 w-12 flex items-center justify-center p-0 lg:h-16 lg:w-16"
                >
                  <img
                    :src="item.imageUrl"
                    class="h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                  />
                </div>
                <div class="text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium">{{ item.name }}</div>
                  <div class="text-xs text-gray-400">{{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.rounded-image {
  border-radius: 50%;
  width: 220px;
  height: 220px;
  object-fit: cover;
}

.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(60px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 300ms;
}
.fadeins-2 {
  animation-delay: 550ms;
}

.img-tech,
.tech {
  transition: transform 0.3s ease;
}

.item-tech:hover .img-tech {
  transform: scale(1.3);
}

.item-tech:hover .tech {
  transform: translateY(-12px);
}
</style>
