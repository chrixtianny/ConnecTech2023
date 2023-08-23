<template>
  <section class="contact-section">
    <div class="contact-title">Contato</div>
      <div class="contact-content">
        <p class="contact-text">Para mais informações sobre o evento ou para entrar em contato, você pode enviar um e-mail para:</p>
        <a href="mailto:bsiconnectsevents@gmail.com" class="contact-link">bsiconnectsevents@gmail.com</a>
        <p class="contact-text">ou para as Coordenadoras:</p>
        <p>
          <a href="mailto:ckss6@aluno.ifal.edu.br" class="contact-link">Christianny - ckss6@aluno.ifal.edu.br</a>
        </p>
        <p>  
          <a href="mailto:smcfs1@aluno.ifal.edu.br" class="contact-link">Samyra - smcfs1@aluno.ifal.edu.br</a>
        </p>
        <div class="telegram-info">
          <p class="contact-text">Você também pode nos contatar no Telegram para obter mais informações:</p>
          <a href="https://t.me/c1995k" target="_blank" class="contact-link">Telegram</a>
        </div>
      </div>
  </section>
    <p class="section-title">Organização</p>
    <section class="section">  
      <div class="logo-section">
        <a href="https://instagram.com/bsiconnects">
          <img src="../assets/bsiconnects.png" alt="Logo dos Criadores" class="logo-image">
        </a>
        <div class="institution">
          <div class="institution-logo">
            <a href="https://www2.ifal.edu.br/">
              <img src="../assets/instituicao.png" alt="Logo da Instituição" class="institution-image">
            </a>
          </div>
        </div>
      </div>
    </section>
</template>
<style scoped>
 
.contact-section {
  max-width: 700px;
  background-color: #f2f2f2;
  padding: 40px 0;
  text-align: center;
  margin: 3% auto;
}

.contact-title {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 20px;
  color: #333;
}

.contact-content {
  max-width: 600px;
  margin: 0 auto;
}

.contact-text {
  font-size: 16px;
  margin-bottom: 10px;
  color: #555;
}

.contact-link {
  font-size: 18px;
  color: #007bff;
  text-decoration: none;
  margin: 2px 10px;
}

.contact-link:hover {
  text-decoration: underline;
}
 .section {
    padding: 40px 20px;
    display: flex;
    flex-direction: row;
    justify-content: center;
 }

.section-title {
    text-align: center;
    font-size: 28px;
    font-family: 'Montserrat', sans-serif;
    font-weight: bold;
    margin-bottom: 20px;
    color: #333; 
    padding: 40px 20px;
  
}

.telegram-info {
  margin-top: 20px;
}

.logo-image{
    max-width: 250px;
    max-height: 150px;
    margin: 5% auto;
    display: block;
}

.institution-image{
    max-width: 250px;
    max-height: 150px;
    margin: 0 auto;
    display: block;
}
</style>