<template>
  <div class="wrap">
    <q-layout view="lHh Lpr lFf">
      <q-layout-header>
        <div class="header">
          <input type="checkbox" id="control-nav" />
          <label for="control-nav" class="control-nav"></label>
          <label for="control-nav" class="control-nav-close"></label>
          <nav class="float-r">
            <ul class="list-auto">
              <li id="NomeHelp">
                <div class="container">
                  <div class="row justify-left q-mr-sm">
                    <div class="col-2">
                      <img id="DevLogo" src="~assets/loguinho01.png" />
                    </div>
                  </div>
                </div>
              </li>
              <li>
                <router-link class="item-menu" :to="{ name: 'Inicio' }">Inicio</router-link>
              </li>
              <li>
                <router-link class="item-menu" :to="{ name: 'quemE' }">Quem é Bruno</router-link>
              </li>
              <li>
                <router-link class="item-menu" :to="{ name: 'projetos' }">Projetos Recentes</router-link>
              </li>
              <li>
                <router-link class="item-menu" :to="{ name: 'curriculo' }">Curriculo</router-link>
              </li>
              <li>
                <router-link class="item-menu" :to="{ name: 'informeAqui' }">Informe Aqui</router-link>
              </li>
              <li>
                <router-link class="item-menu" :to="{ name: 'gitHub' }">GitHub</router-link>
              </li>
            </ul>
          </nav>
        </div>
      </q-layout-header>
      <section>
        <div class="container">
          <div class="row justify-center q-mb-xl">
            <div class="col-12">
              <q-parallax>
                <img id="ImgBanner" slot="media" src="~assets/note02.jpg" />
                <h1 id="CAFe">Portifolio DevIDe></h1>
              </q-parallax>
            </div>
          </div>
        </div>

        <div class="container" style="background:#D3D3D3;">
          <div class="row justify-left q-ma-xl">
            <div class="col-12">
              <h2 id="topico1" class="row justify-center q-ma-xl">Quem é Bruno:</h2>
              <p id="paragrafo" style="text-align: left">
                Graduando em Análise e Desenvolvimento de Sistemas, cursando o quarto período.
                Atualmente trabalho na Universidade de Pernambuco - UPE no NCTI, na parte de Tecnologia, dando
                manutenção aos sites e implementando funcionalidades. Lido muito bem com as adversidades,
                problemas, contratempos, sou comunicativo e tenho muito vontade em crescer e aprender.
                O que mais me encanta na área de tecnologia é saber que sempre você tem um novo desafio,
                assim podendo ser uma pessoa proativa e em busca de novas metas. Faço também curso de inglês no Senac.
                Básicamente um pequeno resumo, onde tento explicar um pouco sobre mim. Conclusão do curso em Dezembro 2019.
              </p>
              <h2 id="topico1" class="row justify-center q-ma-xl">Projetos Recentes:</h2>
              <div class="container" id="avatar">
                <div class="row q-ma-xl justify-center">
                  <div class="col-10">
                    <q-carousel
                      color="white"
                      height="500px"
                      width="600px"
                      animated
                      v-model="slide"
                      arrows
                      navigation
                      infinite
                      autoplay="infinite"
                    >
                      <q-carousel-slide :name="1" img-src="statics/img01.jpg">
                        <div class="absolute-bottom custom-caption">
                          <div class="q-display-1">Projeto Portifolio WEB:</div>
                          <div
                            class="q-headline"
                          >Projeto Desenvolvido com Node.js com o Back-End, Quasar no Front-End e MongoDB</div>
                        </div>
                      </q-carousel-slide>
                      <q-carousel-slide :name="2" img-src="statics/img02.jpg">
                        <div class="absolute-bottom custom-caption">
                          <div class="q-display-1">Projeto Biblioteca em - JAVA</div>
                          <div
                            class="q-headline"
                          >Projeto acadêmico com Java e o banco relacional MySQL.</div>
                        </div>
                      </q-carousel-slide>
                      <q-carousel-slide :name="3" img-src="statics/img03.jpg">
                        <div class="absolute-bottom custom-caption">
                          <div class="q-display-1">Projeto HelpUp Back-End e Front-End</div>
                          <div
                            class="q-headline"
                          >Projeto Desenvolvido na faculdade. Validações JWT, Testes e Front-End</div>
                        </div>
                      </q-carousel-slide>
                      <q-carousel-slide :name="4" img-src="statics/img04.jpg">
                        <div class="absolute-bottom custom-caption">
                          <div class="q-display-1">Tela de Login em Angular</div>
                          <div
                            class="q-headline"
                          >Projeto de uma tela de login, com o FrameWork Angular.</div>
                        </div>
                      </q-carousel-slide>
                    </q-carousel>
                  </div>
                </div>
              </div>
              <div class="container">
                <div class="row q-ma-xl">
                  <div class="col-12">
                    <h2 id="topico1" class="row justify-center q-ma-xl">Currículo e Informações:</h2>
                    <p id="paragrafo" style="text-align: left">
                      Logo abaixo esta meu currículo com uma previa visualização e as opção de impressão
                      ou download. Nele contém todas informações profissionais, ultimos locais de trabalho
                      e o que tenho de conhecimento e cursos. Deixei o mesmo para facilitar o acesso de
                      forma profissional as pessoas que por ventura ficarem interessadas em conhecer um pouco
                      mais dos meus conhecimentos e consequentimente quiserem contratar-me. Nele também tem:
                      meu email, telefone e algumas redes sociais e profissionais.(Linkdin e GitHub)
                    </p>

                    <div class="row justify-center q-mt-xl">
                      <iframe src="statics/CurriculoBruno.pdf" id="curriculo"></iframe>
                    </div>

                    <h2 id="topico1" class="row justify-center q-ma-xl">Conhecimento:</h2>
                    <lis class="paragrafo" style="text-align: left" id="li">
                      <li>Idioma: Inglês no Senac.</li>
                      <li>Curso Extra: Informatica na Unibratec.</li>
                      <li>Web Back-End: Node.js.(POO)</li>
                      <li>Web Front-End: JavaScript, HTML5 e CSS3.</li>
                      <li>Banco de Dados: MySql, SQLServer e MongoDB.</li>
                      <li>Desenvolvimento para Desktop: Java e C#.(POO)</li>
                      <li>Estudo em andamento: React e Angular.</li>
                      <li>FrameWork: Express, Knex, Body-Parse, BootStrap e Quasar.</li>
                    </lis>

                    <h2 id="topico1" class="row justify-center q-ma-xl">Hobby e Preferências:</h2>
                    <lis class="paragrafo" style="text-align: left" id="li">
                      <li>Café - Sou fã de um excelente café. Melhor café em minha opnião, Galo Padeiro.</li>
                      <li>Games - Sempre apreciei um execelente jogo. Sempre fiquei pensando qual e como funcionava toda lógica deles.</li>
                      <li>Música - Por um tempo estudei musica e ela é uma paixão. Ela é um Hobby para acalmar a alma em momentos extressantes.</li>
                      <li>Ler Livros - Ler nos permite além de angariar conhecimento, permite também que possamos viajar sem precisar sair do lugar.</li>
                      <li>Series - Além de gostar do habito, uso para aumentar meu conhecimento no inglês! Coloco Audio e Legenda em inglês.</li>
                      <li>Tecnologia - Sou apaixonado por minha área de atuação, justamente por sempre ter algo novo. Constante aprendizado.</li>
                      <li>Programar - Posso considerar a melhor hora pra mim. É como se fosse um enorme quebra cabeça na vida e aos poucos vamos encaixando. Temos a obrigação de facilitar a vida de outras pessoas e é isso que acho o máximo.</li>
                    </lis>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="container">
          <div class="row justify-center q-ma-xl" style="background:#ffffff">
            <div class="col-6">
              <h2 id="topico1" class="row justify-center q-ma-xl">Informe aqui:</h2>
              <p id="paragrafo" style="text-align: left">
                Aqui você pode nos informar em que nossa aplicação poderia melhorar.
                Assim deixando sua opnião sobre nosso site e cada vez mais melhoraremos
                nossa aplicação. Contamos com sua informação, deixe aqui sua mensagem nos
                avaliando, dando opniões ou até mesmo tirando dúvidas.
              </p>
              <q-input v-model="text" type="Nome" float-label="Nome" placeholder="Nome" />
              <q-input v-model="text" type="Email" float-label="Email" placeholder="Email" />
              <q-input
                v-model="text"
                type="mensagem"
                float-label="Mensagem"
                placeholder="Mensagem Informativa"
              />
              <div class="row justify-center">
                <q-btn
                  class="q-mr-xl q-ml-xl q-mt-md"
                  style="width:50%; height:20px"
                  color="blue"
                  label="Enviar"
                />
              </div>
            </div>
          </div>
        </div>
        <div class="container">
          <div class="row justify-center q-ma-xl">
            <div class="col-12">
              <h2 id="topico1" class="row justify-center q-ma-xl">Principais Projetos:</h2>
            </div>
          </div>
        </div>
        <div class="container">
          <div class="row justify-center q-ma-xl">
            <div class="col-10">
              <q-card inline style="width:260px;">
                <q-card-media>
                  <img src="~assets/node.jpeg" />
                </q-card-media>
                <q-card-title>
                  Projeto Back e Front
                  <q-rating slot="subtitle" v-model="stars" :max="5" />
                  <div slot="right" class="row items-center">
                    <q-icon name="place" />PE
                  </div>
                </q-card-title>
                <q-card-main>
                  <p>Desenvolvimento Web</p>
                  <p class="text-faded">Serviços de cuidadores para idosos.</p>
                </q-card-main>
                <q-card-separator />
              </q-card>
              <q-card inline style="width: 260px;">
                <q-card-media>
                  <img src="~assets/node.jpeg" />
                </q-card-media>
                <q-card-title>
                  Biblioteca em Java
                  <q-rating slot="subtitle" v-model="stars" :max="5" />
                  <div slot="right" class="row items-center">
                    <q-icon name="place" />PE
                  </div>
                </q-card-title>
                <q-card-main>
                  <p>Desenvolvimento Desktop</p>
                  <p class="text-faded">Serviços de cuidadores para idosos.</p>
                </q-card-main>
                <q-card-separator />
              </q-card>
              <q-card inline style="width: 260px;">
                <q-card-media>
                  <img src="~assets/node.jpeg" />
                </q-card-media>
                <q-card-title>
                  Mauricio Chagas
                  <q-rating slot="subtitle" v-model="stars" :max="5" />
                  <div slot="right" class="row items-center">
                    <q-icon name="place" />PE
                  </div>
                </q-card-title>
                <q-card-main>
                  <p>Desenvolvimento Web</p>
                  <p class="text-faded">Serviços de cuidadores para idosos.</p>
                </q-card-main>
                <q-card-separator />
              </q-card>
              <q-card inline style="width: 260px;">
                <q-card-media>
                  <img src="~assets/node.jpeg" />
                </q-card-media>
                <q-card-title>
                  Vitoria Caldas
                  <q-rating slot="subtitle" v-model="stars" :max="5" />
                  <div slot="right" class="row items-center">
                    <q-icon name="place" />PE
                  </div>
                </q-card-title>
                <q-card-main>
                  <p>Desenvolvimento Web</p>
                  <p class="text-faded">Serviço especial com crianças.</p>
                </q-card-main>
                <q-card-separator />
              </q-card>
            </div>
          </div>
        </div>
      </section>

      <footer>
        <!--<div class="footer" id="Contatos">
          <div class="row q-ma-xl justify-center">
            <div class="col-2">
              <h2 id="contato"></h2>
              <div class="row justify-left" id="instagram"></div>
            </div>
          </div>
        </div>-->
      </footer>
      <q-page-container>
        <router-view />
      </q-page-container>
    </q-layout>
  </div>
</template>

<script>
import { openURL } from "quasar";

export default {
  name: "MyLayout",
  data() {
    return {
      leftDrawerOpen: this.$q.platform.is.desktop
    };
  },
  methods: {
    openURL
  }
};
</script>

<style >
</style>
