<script>
// @ts-nocheck

    import Modal from "./modal.svelte";
   
    let modal;
    let modal2;
</script>
<body> 
    <div class="container">
      <h1>PALAVRAS CRUZADAS</h1>
      <p>Bem-vindo! Divirta-se e desafie-se!</p>
      <button><a href="/página do jogo">iniciar jogo</a></button>
      <button on:click={()=>modal.show()}>Informações</button>
      <Modal bind:this={modal}>
        <h2>informações</h2>
        <p>Desenvolvido por: <br>Rebeca vitoria <br>Marilia gabriela <br>Arthur severino <br> Matheus josé <br>José glênio. <br>Com a ajuda do monitor: <br> Cleiton lucas.</p>
        <button on:click={() => modal.hide()}>Fechar</button>
      </Modal>
      <button on:click={()=>modal2.show()}>Instruções</button>
      
      <Modal bind:this={modal2}>
        <h2>instruções</h2>
       <nav>
        <p>Coloque letras minúsculas. <br>Apenas verifique a resposta depois de completar todas as palavras.</p>
       </nav>
       <button on:click={() => modal2.hide()}>Fechar</button>
      </Modal>
     </div>
</body>
      
      <style>
         @font-face {
      font-family: 'glossy';
      src: url('Glossy Sheen Shine DEMO.ttf') format('truetype');
      font-weight: normal;
      font-style: normal;
 }
    .container {
  text-align: center;
  margin-top: 200px;
  font-family: 'glossy';
}
h1 {
  
  font-size: 90px;
  margin-bottom: 20px;
  font-weight: normal;
}
button {
  padding: 10px 20px;
  font-size: 18px;
  background-color: rgb(71, 93, 153);
  color: wheat;
  border: 2px solid #0084ff;
 border-style: inherit;
  border-radius: 4px;
  font-family: 'glossy';
  }
  button:hover{
    box-shadow: 0 0 15px rgb(5, 198, 252), inset 0 0 15px rgb(4, 215, 252);
  }
a{
  color: wheat;
  text-decoration: none;
 }
body{
  background-color: white;
}
nav{
  font-size: 25px;
}
</style>