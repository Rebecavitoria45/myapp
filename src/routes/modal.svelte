<script>
    let shown= false;
   export function show(){
        shown = true;
 }
 export function hide(){
   shown = false;
 }
</script>
<style>
.modal-wrapper{
  background-color: black;
  background-color: rgba(0,0,0,0.6);
  position: fixed;
  width: 100%;
  height: 100%;
  top:0;
  left: 0;
  
}
.modal{
    background-color: whitesmoke;
    max-width: 80vw;
    padding: 1rem;
    margin: 10% auto;

}
</style>
<svelte:window
on:keydown={ (e) => {
    if(e.keyCode == 27){
        hide();
    }
    }}/>

{#if shown}
<div class="modal-wrapper">
 <div class="modal">
     <slot />
    </div>
</div>
{/if}