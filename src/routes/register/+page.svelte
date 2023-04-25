<script>

  let name  = '';
  let email = '';
  let password = '';

  async function cadastrar() {

    const data = { name: name, email: email, password: password };
    const options = {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(data),
    };
    const response = await fetch('http://localhost:3000/api/users', options);
    const responseData = await response.json();
    console.log(responseData);
  }
</script>

<div class="register-container">
  <form>
    <label for="name">Nome completo:</label>
    <input type="text" id="name" name="name" bind:value={name} required />

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" bind:value={email} required />

    <label for="password">Senha:</label>
    <input type="password" id="password" name="password" bind:value={password} required />

    <button type="button" on:click={() => cadastrar()}>Registrar</button>
  </form>

  <p>Já tem uma conta? <a href="/login">Faça login aqui</a>.</p>
</div>

<style>
  .register-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background-color: #f5f5f5;
  }

  form {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    padding: 40px;
    border-radius: 5px;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  }

  label {
    font-weight: bold;
    margin-bottom: 10px;
  }

  input[type="text"],
  input[type="email"],
  input[type="password"],
  input[type="cpf"] {
    width: 100%;
    padding: 10px;
    border: none;
    border-bottom: 2px solid #ccc;
    margin-bottom: 20px;
    font-size: 16px;
    outline: none;
  }

  input[type="text"]:focus,
  input[type="email"]:focus,
  input[type="password"]:focus,
  input[type="cpf"]:focus {
    border-bottom-color: #0077cc;
  }

  button[type="submit"] {
    background-color: #0077cc;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s ease-in-out;
  }

  button[type="submit"]:hover {
    background-color: #004466;
  }

  a {
    color: #0077cc;
    text-decoration: none;
    transition: color 0.3s ease-in-out;
  }

  a:hover {
    color: #004466;
  }
</style>
