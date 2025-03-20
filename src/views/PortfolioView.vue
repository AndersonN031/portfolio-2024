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
          name: 'Website Pessoal',
          imageUrl: 'portfolio_v2',
          status: 'Site pessoal, criado para mostrar meu perfil, habilidades e buscando exibir minhas experiências profissionais. Também um bom lugar para testar novas tecnologias.',
          description: 'Desenvolvi este site pessoal como um portfólio digital utilizando VueJS 3 e Tailwind CSS. Implementei um design responsivo, animações suaves e uma estrutura de components reutilizáveis. O projeto foi deployado na Vercel e serve como showcase das minhas habilidades frontend.',
          tech: 'VueJS 3, Tailwind',
          github: 'https://github.com/AndersonN031/portfolio-2024',
          demo: 'https://devanderson.vercel.app/'
        },
        {
          id: 2,
          name: 'Controle de estoque',
          imageUrl: 'esmercado',
          status: 'Projeto desenvolvido para um comércio local com intuíto de guardar informações na web e ter um controle mais fácil e rápido de seus variáveis produtos.',
          description: 'Criei um sistema de controle de estoque full-stack usando NextJS para o frontend, NodeJS para o backend e MongoDB como banco de dados. Implementei funcionalidades de CRUD para produtos, autenticação de usuário e um dashboard para visualização de estoque.',
          tech: 'NextJS, NodeJS e MongoDB ',
          github: 'https://github.com/AndersonN031/nexjs-mongo-deploy',
          demo: 'null'
        },
        {
          id: 3,
          name: 'CF Obras',
          imageUrl: 'cfobras',
          status: 'CF Obras é um projeto voltado à venda de insumos de grande porte ou em grandes quantidades no ramo da construção civil, atendendo às requisições dos clientes.',
          description: 'Atuei como PJ em um projeto de obras, focando no Back-End para resolver bugs em requisições de insumos dentro de uma arquitetura MVC, garantindo maior confiabilidade e precisão no fluxo de dados do sistema. Implementei essas melhorias no Front-End utilizando React.js para construir telas intuitivas, facilitando a interação dos usuários com o processo de gestão de insumos. Durante a entrega, utilizei tecnologias como React.js, TypeScript, Nest.js e MongoDB, aprimorando a robustez e a escalabilidade da aplicação. Minhas contribuições reduziram falhas operacionais, otimizando o gerenciamento de recursos no projeto de obras.',
          tech: 'VueJS 3, Typescript, NestJS e MongoDB',
          github: 'null',
          demo: 'null'
        },
        {
          id: 4,
          name: 'Portfolio Design gráfico',
          imageUrl: 'design',
          status: 'Freelancer de um portfólio para um designer gráfico/motion para exibir na web sua experiência e projetos.',
          tech: 'ReactJS/NextJS, Css & Bootstrap',
          github: 'null',
          demo: 'https://irton-design.vercel.app/'
        },
        {
          id: 5,
          name: 'Poliglobalizando',
          imageUrl: 'poliglobalizando',
          status: 'Desenvolvedor Full-Stack em um curso de inglês gratuito voltado para apoiar pessoas de baixa renda no aprendizado da língua inglesa.',
          description: 'Atuei como desenvolvedor Full-Stack em um curso de inglês gratuito voltado para apoiar pessoas de baixa renda no aprendizado da língua inglesa. Desenvolvi interfaces dinâmicas utilizando Next.js, garantindo uma experiência acessível e intuitiva que facilitou o engajamento dos alunos, mesmo aqueles com pouca familiaridade com tecnologia. Criei APIs para o gerenciamento de dados com Node.js e Express, além de otimizar bancos de dados relacionais, o que assegurou um acompanhamento eficiente e escalável do progresso dos estudantes. Implementei funcionalidades para cadastro e monitoramento, oferecendo uma experiência personalizada que incentivou a participação ativa dos alunos.',
          tech: 'NextJS, Express & SQL',
          github: 'null',
          demo: 'null'
        },
        {
          id: 6,
          name: 'Gestão de Leads',
          imageUrl: 'leads',
          status: 'Permite adicionar, atualizar, excluir e buscar Leads, com suporte a grupos e campanhas.',
          description: `Projeto de Gerenciamento de Leads: Projeto pessoal 
          desenvolvido exclusivamente para o backend, utilizando TypeScript, Node.js, Express, Prisma, Zod e PostgreSQL. Permite adicionar, atualizar, excluir e buscar Leads, com suporte a grupos e campanhas. Grupos e campanhas podem ser criados, atualizados e removidos, e cada Lead pode ser associado a uma ou mais campanhas e grupos.
          
          O sistema conta com funcionalidades como filtragem avançada e paginação, além de possibilitar a gestão eficiente das associações entre Leads, grupos e campanhas. Com regras de negócio bem definidas, baixo acoplamento e alta coesão, o projeto prioriza escalabilidade e manutenção. O uso de tecnologias modernas, como Prisma para ORM e Zod para validação, garante um backend robusto e confiável, pronto para integração com futuros frontends.`,
          tech: "NodeJS, PostgreSQL, Zod & Prisma",
          github: 'https://github.com/AndersonN031/gest-o-de-leads',
          demo: 'null'
        }

        
      ]
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
    }
  }
}
</script>

<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Experiência</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300">
            Projetos que atuei até o momento</h4>
          </div>
        </header>
        <section>
        <h4 class="text-sm font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-yellow-300 mb-4">Clique no card para ter mais informações!</h4>
        <div>
          <div class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in">
            <div v-for="item in items" :key="item.id">
              <div 
                @click="openModal(item)"
                class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5 cursor-pointer">
                <div class="flex h-12 w-12 items-center justify-center p-0 h-full w-full lg:p-0 zoom-in">
                  <img alt="HTML" loading="lazy" decoding="async" data-nimg="1"
                    class="drop-shadow-xl rounded rounded-xl" :src="'/img/portfolio-' + item.imageUrl + '.png'">
                </div>
                <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                  <div class="title-text font-medium text-secondary">{{ item.name }}</div>
                  <div class="w-full text-left text-[10px] text-[#c1c1c1] md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                  <div class="w-full mt-4 text-normal text-sm text-left text-amber-200">
                    {{ item.tech }}
                  </div>
                  <div class="w-full flex justify-end">
                    <div class="flex cursor-pointer items-end gap-2 text-primary">
                      <a v-if="item.github !== 'null'" :href="item.github" target="_blank" rel="noreferrer"
                        title="View github repository" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24"
                          stroke-linecap="round" stroke-linejoin="round" height="16" width="16"
                          xmlns="http://www.w3.org/2000/svg">
                          <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
                        </svg></a>
                      <a v-if="item.demo !== 'null'" :href="item.demo" target="_blank" rel="noreferrer"
                        title="View finished project" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24"
                          stroke-linecap="round" stroke-linejoin="round" height="18" width="18"
                          xmlns="http://www.w3.org/2000/svg">
                          <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
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

    <!-- Modal -->
    <div v-if="showModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
      <div class="bg-[#1e1e1f] rounded-xl p-6 max-w-lg w-full mx-4 border border-[#383838]">
        <div class="flex justify-between items-center mb-4">
          <h3 class="text-xl font-bold text-amber-50">{{ selectedItem?.name }}</h3>
          <button @click="closeModal" class="text-amber-200 hover:text-amber-400">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
        <div class="text-[#c1c1c1] mb-4">{{ selectedItem?.description }}</div>
        <div class="text-amber-200 mb-4">Tecnologias: {{ selectedItem?.tech }}</div>
        <div class="flex justify-end gap-4">
          <a v-if="selectedItem?.github !== 'null'" :href="selectedItem?.github" target="_blank" 
             class="text-primary hover:text-accent">GitHub</a>
          <a v-if="selectedItem?.demo !== 'null'" :href="selectedItem?.demo" target="_blank" 
             class="text-primary hover:text-accent">Demo</a>
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

/* Animação do modal */
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
  animation: modalFadeIn 0.3s ease-out;
}
</style>