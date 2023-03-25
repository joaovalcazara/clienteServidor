<script>

    const signin = () =>{

    }
  </script>
  
    <div class="login-container">
        <form on:submit|preventDefault={signin} class="lg:w-2/6 md:w-1/2 bg-gray-100 rounded-lg p-8 flex flex-col w-full mt-10 md:mt-0 ">
            <label for="username">Nome de usuário:</label>
            <input type="text" id="username" name="username" required>
    
            <label for="password">Senha:</label>
            <input type="password" id="password" name="password" required>
    
            <button type="submit">Entrar</button>
      </form>
  
      <p>Não tem uma conta? <a href="/register">Registre-se aqui</a>.</p>
    </div>
  
  <style>
    .login-container {
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
    input[type="password"] {
      width: 100%;
      padding: 10px;
      border: none;
      border-bottom: 2px solid #ccc;
      margin-bottom: 20px;
      font-size: 16px;
      outline: none;
    }
  
    input[type="text"]:focus,
    input[type="password"]:focus {
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
  