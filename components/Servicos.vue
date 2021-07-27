<template>
  <section class="container w-3/5 text-justify" style="padding-top: 4vw; padding-left: 4vw;">
  <hr style="height: 10vw;" />
  <h2>Nossos clientes e parceiros</h2>
  <div style="display: flex; flex-direction: row; justify-content: space-between;" >
  <div style="padding: 2vw;" v-for="(servico, index) in this.servicos" :key="index">
    <div>
    <a :href="servico.link">
    <h1 class="z-50" style="width: 10vw; margin-bottom: -4vw; position: relative; color: var(--thirdy-color)"><b>{{servico.nome}}</b></h1>
    <nuxt-img class="z-10" style="width: 20vw; height: 20vw; border-radius: 1vw; position: relative;" :src="servico.img" />
    </a>
    </div>

    </div>
  </div>
  <hr style="height: 10vw;" />
  </section>
</template>
<script>
export default {
  data(){
    return{
    servicos:[
      {nome: "Eyevision Mídias Interativas", link: "http://eyevision.ai/", img: "/clientes/eyevisionprint.jpg"}
    ]
    }
  }
}
</script>
