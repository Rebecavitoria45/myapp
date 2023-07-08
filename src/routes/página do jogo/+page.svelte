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
		[0,0,0,0,0,0,0,0,0,"C"],
		[0,0,0,0,0,"H","A","R","P","A"],
		[0,0,0,0,0,0,0,0,0,"L"],
		["V","O","A","R",0,"H","O","M","E","M"],
		[0,0,0,"E",0,0,0,"E",0,"O"],
		[0,"I","N","V","E","J","O","S","O",0],
		[0,0,0,"I",0,0,0,"A",0,0],
		[0,0,"I","D","E","A","L",0,0,0],
		[0,0,0,"A",0,0,0,0,0,0],
		[0,0,0,"R",0,0,0,0,0,0],
		]
		
	 
		var input= ""
	
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
                    
					<input  type="texto" id="celula" bind:value={resposta[i][j]} maxlength="1"  class="branco" style="background-color: {input}" /> 
					
					{/if}	
					</td>
				{/each}
			</tr>
		{/each}
       
     
	</table>
    
  

    </div>
<div class="horizontal">
        <h2>Horizontal</h2>
<p>1. Aquele que tem inveja  (8 LETRAS)</p>

<p>4.Individuo do sexo masculino (5 LETRAS)</p>

<p>5. o que é objeto da nossa mais alta aspiração: a solução perfeita (5 LETRAS)</p>

<p>7. Instrumento bastante antigo, composto de cordas estendidas numa moldura aberta (5 LETRAS) </p>

<p>8.Mover-se ou sustentar-se no ar por meio de asas ou algum meio mecânico <br>(4 LETRAS)</p>
<h2>Vertical</h2>
<p> 2.Vingar uma agressão com outra maior,mais violenta (7 LETRAS)</p>

<p>3. Móvel destinado a refeiçôes,jogos,apoio etc (4 LETRAS)</p>

<p>6. Quieto, sossegado: não apresenta agitação, pertubação <br>(5 LETRAS)</p>
<button on:click={()=> compareArrays()}>Verificar</button>



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
    .horizontal{
        

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
 
  
  
	</style>
