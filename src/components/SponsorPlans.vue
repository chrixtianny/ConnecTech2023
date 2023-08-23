<template>
  <section class="plans">
    <v-row rows="2">
      <v-card class="sponsoring-plans" v-for="plan in plans_data" :key="plan.id">
        <div class="plan-content">
          <div class="plan-details">
            <img class="icon-plans" :src="plan.imgLink" :alt="plan.title" style="max-height: 100px;">
            <div class="plan-title">{{ plan.title }}</div>
            <div class="plan-amount">{{ formatCurrency(plan.amount) }}</div>
            <div class="benefit-card" v-for="benefit in plan.benefits" :key="benefit.id">
              <div class="benefit-icon">
                <v-icon>{{ benefit.palestras }}</v-icon> Palestras de Tema Livre*</div>
                <div class="benefit-icon">
                <v-icon>{{ benefit.video }}</v-icon> Exibição de Vídeo</div>
                <div class="benefit-icon">
                <v-icon>{{ benefit.banner }}</v-icon> Banner</div>
                <div class="benefit-icon">
                <v-icon>{{ benefit.marketing }}</v-icon> Logotipo no Certificado</div>
                <div class="benefit-icon">
                <v-icon>{{ benefit.logotipo }}</v-icon> Logotipo no Site</div>
                <div class="benefit-icon">
                <v-icon>{{ benefit.mencao }}</v-icon> Menção no Cerimonial
              </div>
            </div>
          </div>
        </div>
      </v-card>
    </v-row>
  </section>
</template>

<script setup>

  const plans_data = [
    {
      id: 1,
      title: 'Diamante',
      amount: 2000,
      imgLink: "https://ibb.co/qMD4gBM",
      benefits: [
        {
          palestras: "mdi-check-circle-outline",
          video: "mdi-check-circle-outline",
          banner: "mdi-check-circle-outline",
          marketing: "mdi-check-circle-outline",
          logotipo:  "mdi-check-circle-outline",
          mencao: "mdi-check-circle-outline",
        },
      ], },
      {
      id: 2,
      title: 'Ouro',
      amount: 1000,
      imgLink: "https://ibb.co/jgBDy5d",
      benefits: [
        {
          palestras: "mdi-cancel",
          video: "mdi-check-circle-outline",
          banner: "mdi-check-circle-outline",
          marketing: "mdi-check-circle-outline",
          logotipo:  "mdi-check-circle-outline",
          mencao: "mdi-check-circle-outline",
        },],},
        {
      id: 3,
      title: 'Prata',
      amount: 500,
      imgLink: "https://ibb.co/9ttwPKJ",
      benefits: [
        {
          palestras: "mdi-cancel",
          video: "mdi-cancel",
          banner: "mdi-check-circle-outline",
          marketing: "mdi-check-circle-outline",
          logotipo:  "mdi-check-circle-outline",
          mencao: "mdi-check-circle-outline",
        },],},
      {
      id: 4,
      title: 'Bronze',
      amount: 250,
      imgLink: "https://ibb.co/xgn4w9B",
      benefits: [
        {
          palestras: "mdi-cancel",
          video: "mdi-cancel",
          banner: "mdi-cancel",
          marketing: "mdi-cancel",
          logotipo:  "mdi-check-circle-outline",
          mencao: "mdi-check-circle-outline",
        },],},

  ];

  function formatCurrency(amount) {
    return `R$ ${amount.toFixed(2)}`;
  }

</script>

<style scoped>

.plans {
  padding: 10px;
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
}

.icon-plans{
  height: 100vh;
  max-height: 100px;
  max-width: 100px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

div.v-row{
  width: 900px;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
}

.sponsoring-plans {
  background-color: #e3d9e6;
  width: 250px;
  height: 400px;
  border-radius: 2%;
  padding: 15px;
  margin: 10px;
  display: flex;
  text-align: left;
  font-family: 'Montserrat', sans-serif;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  color: rgb(39, 4, 34);
  transition: transform 0.3s;
}

.sponsoring-plans:hover {
  transform: scale(1.06);
  background-color: #9d91a5;
}

.plan-title {
  font-size: 28px;
  font-weight: bold;
  margin-bottom: 10px;
  text-align: center;
}

.plan-amount {
  font-size: 21px;
  font-weight: bold;
  padding: 10px 0; 
  text-align: center;
}
</style>
