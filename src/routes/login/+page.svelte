<script>
// @ts-nocheck

let username = ""
let password = ""
  const signin = () => {
    console.log("ola")
  }
</script>

<form on:submit|preventDefault={signin} class="lg:w-2/6 md:w-1/2 bg-gray-100 rounded-lg p-8 flex flex-col w-full mt-10 md:mt-0 ">
    <div class="formLogin">
        <a href="/">Voltar</a>
        <div class="flex justify-between textoLogin">
            <h2 class="text-gray-900 text-lg font-medium title-font mb-5">Login</h2>
        </div>
        <div class="row">
            <div class="inputs">
                <input label="Username" bind:value={username} type="text" required />
    
            </div>
            <div  class="inputs">
                <input label="Password" bind:value={password} type="password" required />
            </div>
    
        </div>
       <button class="buttonEntrar">Entrar</button>
       <a  class="buttonEntrar" href="/register">Registrar</a>

    </div>
   

</form>


<style>
 .inputs{
    margin-top: 4px;
    margin-left: 40%;
 }
 .textoLogin{
    margin-top: 4px;
    margin-left: 44%;
    text-align: justify;
 }
 .buttonEntrar{
    margin-top: 10px;
    margin-left: 45%;
    text-align: justify;
    font-family: Arial, Helvetica, sans-serif;
    display: block;
 }
 .formLogin{
    margin-top: 10%;
    background-color: antiquewhite;
 }
</style>