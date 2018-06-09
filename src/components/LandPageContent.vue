<template>
  <div>
    <section id='sobre'>
    <div class="container">
      <h3>Fácil. Intuitivo. Simples. Transparente.</h3>
      <p>
        Falha na comunicação, Assembléias Extensas, Livros de Papel e etc.
        Nós não queremos isso! Nós simplificamos tudo isso para você. <br>
        Construímos uma plataforma que oferece transparência, eficiência e simplicidade para o seu condomínio.
      </p>
    </div>
    </section> 
    <section class="inverse blue services"> 
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-sm-12" v-bind:key="index" v-for="(service, index) in services">
            <div class="service">
              <div class="row align-items-center">
                <div class="col-2 text-center">
                  <i v-bind:class="['icon', service.icon]"></i>
                </div>
                <div class="col">
                  <h4>{{service.title}}</h4>
                  <p>{{service.content}}</p>
                </div>
              </div>
            </div>        
          </div>
        </div>
      </div>
    </section>
    <section>
      <div class="container" v-if="!form.joined">
        <h3>Cadastre seu email e receba novidades sobre o projeto.</h3>
        <div class="row">
          <div class="col">
            <b-form v-on:submit="joinEmail($event)">
              <b-input-group>
                <b-form-input 
                  id="exampleInput1"
                  type="email"
                  v-model="form.email"
                  size="lg"
                  required
                  placeholder="Informe o seu email">
                </b-form-input>
                <b-input-group-append>
                  <b-btn variant="primary" size="lg">Cadastrar</b-btn>
                </b-input-group-append>
              </b-input-group>              
            </b-form>
          </div>
        </div>
      </div>
      <div class="container" v-if="form.joined">
        <h3>Obrigado por cadastrar seu email, lhe manteremos informado!</h3>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'LandPageContent',
  data () {
    return {
      form: {
        email: '',
        joined: false
      },
      services: [
        {
          icon: 'icon-calendar',
          title: 'Reservas',
          content: 'Faça a sua reserva da sua área de lazer no melhor dia e horário disponível. Se precisar, cancele sua reserva, sem complicações.'
        },
        {
          icon: 'icon-book',
          title: 'Ocorrências',
          content: 'Cadastre suas reclamações e seja notificado quando a ocorrência for resolvida. Tudo de forma simples e eficiente. Seu livro de ocorrência virtual.'
        },
        {
          icon: 'icon-info',
          title: 'Informativos',
          content: 'Tenha praticidade e otimize sua comunicação enviando informações importantes para que seus condôminos. Seja notificado quando um novo informativo for postado.'
        },
        {
          icon: 'icon-document',
          title: 'Documentos',
          content: 'Tenha acesso aos documentos relevantes sempre à disposição dos condôminos de forma fácil e transparente. Praticidade no envio das prestações de contas e atas de reunião para consulta dos condôminos.'
        },
        {
          icon: 'icon-selected',
          title: 'Votação',
          content: 'Eficiência para tomar decisões com tranquilidade e transparência. Ganhe tempo nas votações de assembléias e crie enquetes de forma simples e prática.'
        },
        {
          icon: 'icon-barcode',
          title: 'Segunda Via do Boleto',
          content: 'Faça solicitações para emitir a segunda via dos boletos, permitindo autonomia ao condômino.'
        },
        {
          icon: 'icon-settings',
          title: 'Agenda de Manutenção',
          content: 'Tenha controle das manutenções periódicas. Os condôminos serão notificados do status da manutenção.'
        },
        {
          icon: 'icon-build',
          title: 'Localize Serviços',
          content: 'Tenha acesso a lista de prestadores de serviço de sua confiança para o seu condomínio e faça a avaliação dos serviços.'
        }
      ]
    }
  },
  methods: {
    joinEmail: function($event){
      $event.preventDefault()
      console.log(this, this.form)
      this.form.joined = true
    }
  }
}
</script>
