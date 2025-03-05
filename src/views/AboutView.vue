<script>
export default {
  data() {
    return {
      activeTab: 1,
      frontend: [
        { id: 1, name: 'HTML', imageUrl: 'https://cdn-icons-png.flaticon.com/512/1051/1051277.png', status: 'Marcação' },
        { id: 2, name: 'CSS', imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732190.png', status: 'Cascading Style' },
        { id: 3, name: 'Bootstrap', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/bootstrap/bootstrap-original.svg', status: 'Framework' },
        { id: 4, name: 'Sass', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/sass/sass-original.svg', status: 'Extensão do CSS' },
        { id: 5, name: 'Javascript', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-plain.svg', status: 'Programação' },
        { id: 6, name: 'Typescript', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-plain.svg', status: 'Programação' },
        { id: 7, name: 'ReactJS', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg', status: 'Biblioteca' },
        { id: 8, name: 'NextJS', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-plain.svg', status: 'Framework' },
        { id: 5, name: 'WordPress', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/wordpress/wordpress-plain.svg', status: 'CMS' }
      ],
      backend: [
        { id: 1, name: 'NodeJS', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg', status: 'V8 Engine' },
        { id: 2, name: 'Express', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/express/express-original.svg', status: 'Framework' },
        { id: 3, name: 'MongoDB', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mongodb/mongodb-original.svg', status: 'Banco de dados' },
        { id: 4, name: 'PostgreSQL', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg', status: 'Banco de dados' },
        { id: 4, name: 'Prisma', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/prisma/prisma-original.svg', status: 'ORM' },
        
      ],
      tools: [
        { id: 1, name: 'Git', imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png', status: 'Controle de versão' },
        { id: 2, name: 'GitHub', imageUrl: 'https://cdn-icons-png.flaticon.com/512/25/25231.png', status: 'Git Hosting' },
        { id: 3, name: 'NPM', imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png', status: 'Ger. de pacotes' },
        { id: 4, name: 'VSCode', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vscode/vscode-original.svg', status: 'IDE' },
        { id: 5, name: 'Postman', imageUrl: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postman/postman-plain.svg', status: 'API Client' }
      ]
    };
  }
}
</script>

<template>
  <div
  class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5">
  <article data-page="about">

    <header>
      <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
        Sobre mim &nbsp;
        <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left"
          data-aos-duration="600"></div>
      </div>
    </header>

    <section
      class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center">
      <div class="flex justify-center">
        <img alt="avatar" width="300" height="300" src="../images/ANDERSON_08.jpg" class="rounded-image">
      </div>
      <div class="md:w-7/12">
        <p class="mb-3 md:mb-7 fadein-left fadeins-1">
          &nbsp; &nbsp; &nbsp; Olá, sou Anderson Nunes e tenho 21 anos. Com experiência em desenvolvimento para Web, tenho sólidos conhecimentos na aplicação de técnicas avançadas
          de otimização. Comprometido com a criação de soluções eficientes e responsivas, integro constantemente as
          melhores práticas para garantir desempenho e usabilidade excepcionais em todos os projetos. Tenho experiência
          com as principais tecnologias do mercado, incluindo React, Node e SQL

        </p>
        <p class="mb-3 fadein-left fadeins-2">
          &nbsp; &nbsp; &nbsp;
        </p>
      </div>

    </section>

  </article>
</div>
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
          <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 mb-5">
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 1 }"
                @click="activeTab = 1">Front-End</button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 2 }"
                @click="activeTab = 2">Back-End</button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 3 }"
                @click="activeTab = 3">Ferramentas</button>
            </li>
          </ul>
        </div>

        <div v-show="activeTab === 1">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 xl:grid-cols-4">
            <div v-for="item in frontend" :key="item.id">
              <div class="item-tech flex items-center gap-2 border border-amber-200 p-2 hover:bg-amber-200 hover:bg-opacity-10">
                <div class="h-12 w-12 flex items-center justify-center p-0 lg:h-16 lg:w-16">
                  <img :src="item.imageUrl" class="h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]">
                </div>
                <div class="text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium">{{ item.name }}</div>
                  <div class="text-xs text-gray-400">{{ item.status }}</div> <!-- Adicionando o status -->
                </div>
              </div>
            </div>
          </div>
        </div>

        <div v-show="activeTab === 2">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 xl:grid-cols-4">
            <div v-for="item in backend" :key="item.id">
              <div class="item-tech flex items-center gap-2 border border-amber-200 p-2 hover:bg-amber-200 hover:bg-opacity-10">
                <div class="h-12 w-12 flex items-center justify-center p-0 lg:h-16 lg:w-16">
                  <img :src="item.imageUrl" class="h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]">
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
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 xl:grid-cols-4">
            <div v-for="item in tools" :key="item.id">
              <div class="item-tech flex items-center gap-2 border border-amber-200 p-2 hover:bg-amber-200 hover:bg-opacity-10">
                <div class="h-12 w-12 flex items-center justify-center p-0 lg:h-16 lg:w-16">
                  <img :src="item.imageUrl" class="h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]">
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
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 500ms;
}

.fadeins-2 {
  animation-delay: 800ms;
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

.item-tech:hover .status-tech {
  opacity: 1;
}
</style>
