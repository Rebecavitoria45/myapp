<script>
	
let resposta= [
		 [0,0,0,0,0,0,0,0,0,""],
		[0,0,0,0,0,"","","","",""],
		[0,0,0,0,0,0,0,0,0,""],
		["","","","",0,"","","","",""],
		[0,0,0,"",0,0,0,"",0,""],
		[0,"","","","","","","","",0],
		[0,0,0,"",0,0,0,"",0,0],
		[0,0,"","","","","",0,0,0],
		[0,0,0,"",0,0,0,0,0,0],
		[0,0,0,"",0,0,0,0,0,0],
		]
	 let tabela = [
		[0,0,0,0,0,0,0,0,0,"c"],
		[0,0,0,0,0,"h","a","r","p","a"],
		[0,0,0,0,0,0,0,0,0,"l"],
		["v","o","a","r",0,"h","o","m","e","m"],
		[0,0,0,"e",0,0,0,"e",0,"o"],
		[0,"i","n","v","e","j","o","s","o",0],
		[0,0,0,"i",0,0,0,"a",0,0],
		[0,0,"i","d","e","a","l",0,0,0],
		[0,0,0,"a",0,0,0,0,0,0],
		[0,0,0,"r",0,0,0,0,0,0],
		]

	var input= "" ;
	
	function compareArrays() {  
	for (let i = 0; i < resposta.length; i++) {
      for (let j = 0; j < resposta[0].length; j++) {
        if (resposta[i][j] !== tabela[i][j]) {
         console.log(false);
		 return input= "red";
		
        }
    }
 }
 return input= "green";
}
</script>
<!-- var input serve para deixar verde ou vermelha a tabela quando comparado os dois arrays -->
	<div>
        <h1>
            PALAVRA CRUZADA
        </h1>
    </div>	
    
  <div class="tabela">
	<table>
       {#each resposta as linha, i}
			<tr>
				{#each linha as coluna, j}
					<td>
					{#if resposta[i][j]===0}
					<div id="vazio"/>
					{:else}
                    
					<input  type="texto"  autocomplete="off" id="celula" bind:value={resposta[i][j]} maxlength="1"  class="branco" style="background-color: {input}" /> 
					
					{/if}	
					</td>
				{/each}
			</tr>
		{/each}
       </table> <!-- criação da tabela -->
	<button on:click={()=> compareArrays()}>Verificar</button>
  </div>
  
<div class="dicas">

        <h2>Vertical</h2>
<p> Vingar uma agressão com outra maior,mais violenta (7 LETRAS)</p>
<p> Móvel destinado a refeiçôes,jogos,apoio etc (4 LETRAS)</p>
<p>Quieto, sossegado: não apresenta agitação, pertubação <br>(5 LETRAS)</p>
        <h2>Horizontal</h2>
<p> Aquele que tem inveja  (8 LETRAS)</p>
<p>Individuo do sexo masculino (5 LETRAS)</p>
<p> O que é objeto da nossa mais alta aspiração: a solução perfeita (5 LETRAS)</p>
<p>Instrumento bastante antigo, composto de cordas estendidas numa moldura aberta (5 LETRAS) </p>
<p>Mover-se ou sustentar-se no ar por meio de asas ou algum meio mecânico <br>(4 LETRAS)</p>
 <div id="voltar"> <button> <a href="/">Voltar ao menu</a></button> </div> 


</div>
	
<style>
td{
    border: 1px solid white;
    width: 30px;
    height: 30px;
}
input{
    width: 40px;
    height: 40px;
    box-shadow: 0 0 0 0;
    outline: 0;
    text-align: center;
}
table{
    border-collapse: collapse;
    padding-right: 400px;
}
input:focus{
background-color: yellow;
}
@font-face {
font-family: 'glossy';
src: url('Glossy Sheen Shine DEMO.ttf') format('truetype');
font-weight: normal;
font-style: normal;
}
h1{
font-family: 'glossy';
text-align: center;
}
.tabela{
float: right;
padding-right: 200px;
}
.dicas{
text-align: left;
font-family: 'Times New Roman', Times, serif;
border: 5px solid rgb(71, 93, 153);
height: 500px;
width: 550px;
font-size: 17px;
padding-left: 3px;
}
button {
margin-left: 10px;
font-size: 29px;
background-color: rgb(71, 93, 153);
color: rgb(241, 239, 233);
border: 2px solid #0084ff;
border-style: inherit;
border-radius: 4px;
font-family: 'glossy';
}
button:hover{
box-shadow: 0 0 15px rgb(5, 198, 252), inset 0 0 15px rgb(4, 215, 252);
}
a{
	text-decoration: none;
	color: white;
}
#voltar{
	float: right;
}


</style>	
   
	
