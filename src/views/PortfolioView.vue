<script>
export default {
  data() {
    return {
      activeTab: 1,
      showModal: false,
      selectedItem: null,
      items: [
        {
          id: 1,
          name: "Ficha Fácil (em desenvolvimento)",
          imageUrl: "fichafacil",
          status:
            "Sistema de fila virtual para postos de saúde públicos — elimina a necessidade de madrugadas em filas presenciais.",
          description:
            "Projeto pessoal full-stack com foco social. Digitaliza o processo de distribuição de fichas em postos de saúde públicos, permitindo que pacientes entrem na fila virtual pelo celular e acompanhem sua posição em tempo real — sem precisar comparecer presencialmente.",
          bullets: [
            "Arquitetura monolito modular com NestJS — cada operação é um usecase isolado (RegisterUseCase, EnterQueueUseCase…)",
            "Fila virtual com Socket.io para atualização de posição em tempo real",
            "Cache e controle de idempotência com Redis",
            "Autenticação JWT com access token (30min) + refresh token (7d) e RBAC com Guards",
            "Frontend em Next.js 14 com App Router, shadcn/ui e Socket.io Client",
            "Múltiplos papéis: Paciente, Recepcionista, Médico e Admin",
          ],
          tech: "NestJS, Next.js, Redis e PostgreSQL",
          techList: [
            "NestJS",
            "TypeScript",
            "Next.js 14",
            "Prisma",
            "PostgreSQL",
            "Redis",
            "Socket.io",
            "Docker",
          ],
          github: "https://github.com/AndersonN031/ficha-facil-backend/blob/dev/README.md",
          demo: "null",
        },
        {
          id: 2,
          name: "Like Delivery",
          imageUrl: "delivery",
          status:
            "atuando no core de uma plataforma de delivery com sistema de carrinho em tempo real via WebSocket.",
          description:
            "atuando no core de uma plataforma de delivery com sistema de carrinho em tempo real via WebSocket e Redis, autenticação JWT + Twilio e arquitetura hexagonal com NestJS e PostgreSQL.",
          bullets: [
            "Foco principal em Back-End, desenvolvendo APIs, regras de negócio e integrações",
            "Core de plataforma de delivery: pedidos, produtos, categorias e empresas com Arquitetura Hexagonal",
            "Sistema de carrinho em tempo real com WebSocket (Socket.IO) e Redis para cache e sincronização",
            "Autenticação completa com JWT e Twilio (validação via SMS)",
            "Frontend com Next.js (SSR), Zustand, Zod, Shadcn UI e Radix UI",
          ],
          tech: "NextJS, NodeJS e PostgreSQL",
          techList: [
            "NestJS",
            "TypeScript",
            "Prisma",
            "PostgreSQL",
            "Docker",
            "Redis",
            "WebSocket",
            "Next.js",
          ],
          github: "null",
          demo: "null",
        },
        {
          id: 3,
          name: "CF Obras",
          imageUrl: "cfobras",
          status:
            "Plataforma de venda de insumos para construção civil em grandes quantidades.",
          description:
            "Atuei como PJ no projeto, focando em correções de bugs críticos no backend e desenvolvimento de interfaces para gestão de insumos da construção civil.",
          bullets: [
            "Correção de bugs em fluxos de requisição com arquitetura MVC",
            "Interfaces de gestão de insumos com React.js e TypeScript",
            "Integração backend com NestJS e MongoDB",
            "Redução de falhas operacionais no fluxo de dados",
          ],
          tech: "VueJS 3, Typescript, NestJS e MongoDB",
          techList: ["React.js", "TypeScript", "NestJS", "MongoDB"],
          github: "null",
          demo: "null",
        },
        {
          id: 4,
          name: "Portfólio Design Gráfico",
          imageUrl: "design",
          status:
            "Portfólio freelancer para designer gráfico/motion exibir projetos na web.",
          description:
            "Desenvolvimento freelancer de portfólio web para designer gráfico e motion designer, com foco em apresentação visual dos projetos e experiência profissional do cliente.",
          bullets: [
            "Layout moderno e responsivo com Next.js",
            "Galeria de projetos de design",
            "Deploy na Vercel",
          ],
          tech: "ReactJS/NextJS, Css & Bootstrap",
          techList: ["React.js", "Next.js", "CSS", "Bootstrap"],
          github: "null",
          demo: "https://irton-design.vercel.app/",
        },
        {
          id: 5,
          name: "Ren Lab",
          imageUrl: "renlab",
          status:
            "Plataforma de vendas de cursos com integração de pagamentos.",
          description:
            "Website para venda de cursos online da Ren Lab, com integração ao Mercado Pago para processamento de pagamentos e gestão de acesso aos conteúdos.",
          bullets: [
            "Integração com Mercado Pago para pagamentos",
            "Landing page de conversão de cursos",
            "Interface moderna e responsiva",
          ],
          tech: null,
          techList: [],
          github: "null",
          demo: "https://renlabeducacional.com.br/",
        },
        {
          id: 6,
          name: "DLS Academy",
          imageUrl: "dls",
          status:
            "Plataforma de cursos profissionalizantes para capacitação em áreas específicas.",
          description:
            "Website para academia focada em venda de cursos de profissionalização. Interface de alta conversão para apresentação e venda dos cursos disponíveis.",
          bullets: [
            "Landing page orientada à conversão",
            "Apresentação de cursos e instrutores",
            "Interface responsiva e moderna",
          ],
          tech: null,
          techList: [],
          github: "null",
          demo: "https://dlsacademy.com.br/",
        },
      ],
    };
  },
  methods: {
    openModal(item) {
      this.selectedItem = item;
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
      this.selectedItem = null;
    },
  },
};
</script>

<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col"
        >
          <h4>Experiência</h4>
          <h4
            class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300"
          >
            Projetos que atuei até o momento
          </h4>
        </div>
      </header>

      <section>
        <h4
          class="text-sm font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-yellow-300 mb-4"
        >
          Clique no card para ter mais informações!
        </h4>
        <div>
          <div
            class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in"
          >
            <div v-for="item in items" :key="item.id">
              <div
                @click="openModal(item)"
                class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5 cursor-pointer h-full"
              >
                <div
                  class="flex h-12 w-12 items-center justify-center p-0 h-full w-full lg:p-0 zoom-in"
                >
                  <img
                    alt="projeto"
                    loading="lazy"
                    decoding="async"
                    class="drop-shadow-xl rounded rounded-xl"
                    :src="'/img/portfolio-' + item.imageUrl + '.png'"
                  />
                </div>
                <div
                  class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg"
                >
                  <div class="title-text font-medium text-secondary">
                    {{ item.name }}
                  </div>
                  <div
                    class="w-full text-left text-[10px] text-[#c1c1c1] md:text-xs lg:text-sm"
                  >
                    {{ item.status }}
                  </div>

                  <!-- Tech badges -->
                  <div
                    v-if="item.tech"
                    class="w-full mt-2 flex flex-wrap gap-1"
                  >
                    <span
                      v-for="t in item.techList"
                      :key="t"
                      class="px-2 py-0.5 text-[10px] rounded-full bg-amber-200 bg-opacity-10 text-amber-200 border border-amber-200 border-opacity-20"
                    >
                      {{ t }}
                    </span>
                  </div>

                  <div class="w-full flex justify-end mt-2">
                    <div
                      class="flex cursor-pointer items-end gap-2 text-primary"
                    >
                      <a
                        v-if="item.github !== 'null'"
                        :href="item.github"
                        target="_blank"
                        rel="noreferrer"
                        title="Ver repositório no GitHub"
                        @click.stop
                        class="transition-all hover:text-accent"
                      >
                        <svg
                          stroke="currentColor"
                          fill="none"
                          stroke-width="2"
                          viewBox="0 0 24 24"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          height="16"
                          width="16"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"
                          ></path>
                        </svg>
                      </a>
                      <a
                        v-if="item.demo !== 'null'"
                        :href="item.demo"
                        target="_blank"
                        rel="noreferrer"
                        title="Ver projeto ao vivo"
                        @click.stop
                        class="transition-all hover:text-accent"
                      >
                        <svg
                          stroke="currentColor"
                          fill="none"
                          stroke-width="2"
                          viewBox="0 0 24 24"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          height="18"
                          width="18"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"
                          ></path>
                          <polyline points="15 3 21 3 21 9"></polyline>
                          <line x1="10" y1="14" x2="21" y2="3"></line>
                        </svg>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>

    <!-- Modal melhorado -->
    <div
      v-if="showModal"
      class="fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50 px-4"
      @click.self="closeModal"
    >
      <div
        class="bg-[#1e1e1f] rounded-xl max-w-lg w-full border border-[#383838] modal-animation overflow-hidden"
      >
        <!-- Header do modal -->
        <div
          class="flex justify-between items-center px-6 pt-6 pb-4 border-b border-[#383838]"
        >
          <div>
            <h3 class="text-xl font-bold text-amber-50">
              {{ selectedItem?.name }}
            </h3>
          </div>
          <button
            @click="closeModal"
            class="text-[#888] hover:text-amber-200 transition-colors"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>

        <!-- Corpo do modal -->
        <div class="px-6 py-5 space-y-4">
          <!-- Descrição -->
          <p class="text-[#c1c1c1] text-sm leading-relaxed">
            {{ selectedItem?.description }}
          </p>

          <!-- O que foi feito -->
          <div v-if="selectedItem?.bullets?.length">
            <h4
              class="text-xs font-semibold text-[#888] uppercase tracking-widest mb-2"
            >
              O que foi feito
            </h4>
            <ul class="space-y-1">
              <li
                v-for="bullet in selectedItem.bullets"
                :key="bullet"
                class="flex gap-2 text-sm text-[#c1c1c1]"
              >
                <span class="text-amber-400 mt-0.5 flex-shrink-0">▸</span>
                {{ bullet }}
              </li>
            </ul>
          </div>

          <!-- Tecnologias -->
          <div v-if="selectedItem?.techList?.length">
            <h4
              class="text-xs font-semibold text-[#888] uppercase tracking-widest mb-2"
            >
              Tecnologias
            </h4>
            <div class="flex flex-wrap gap-2">
              <span
                v-for="t in selectedItem.techList"
                :key="t"
                class="px-3 py-1 text-xs rounded-full bg-amber-200 bg-opacity-10 text-amber-200 border border-amber-200 border-opacity-20"
              >
                {{ t }}
              </span>
            </div>
          </div>
        </div>

        <!-- Footer do modal -->
        <div class="flex justify-end gap-3 px-6 pb-6">
          <a
            v-if="selectedItem?.github !== 'null'"
            :href="selectedItem?.github"
            target="_blank"
            class="flex items-center gap-2 px-4 py-2 text-sm border border-[#383838] rounded-lg text-[#c1c1c1] hover:border-amber-200 hover:text-amber-200 transition-all"
          >
            <svg
              stroke="currentColor"
              fill="none"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke-linecap="round"
              stroke-linejoin="round"
              height="14"
              width="14"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"
              ></path>
            </svg>
            GitHub
          </a>
          <a
            v-if="selectedItem?.demo !== 'null'"
            :href="selectedItem?.demo"
            target="_blank"
            class="flex items-center gap-2 px-4 py-2 text-sm bg-amber-400 text-black font-semibold rounded-lg hover:bg-amber-300 transition-all"
          >
            <svg
              stroke="currentColor"
              fill="none"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke-linecap="round"
              stroke-linejoin="round"
              height="14"
              width="14"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"
              ></path>
              <polyline points="15 3 21 3 21 9"></polyline>
              <line x1="10" y1="14" x2="21" y2="3"></line>
            </svg>
            Ver Demo
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.item-card:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
}

svg:hover {
  stroke: #ffdb70;
}

@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}

@keyframes modalFadeIn {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.modal-animation {
  animation: modalFadeIn 0.25s ease-out;
}
</style>
