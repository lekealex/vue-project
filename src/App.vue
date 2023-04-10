<template>
    <div class="formulario">
      <form @submit.prevent="enviarFormulario">     
        
          <h1>Formulário de Cadastro</h1>

            <label for="nome">Nome:</label>
            <input type="text" id="nome" v-model="nome">
            <label for="dataNascimento">Data de Nascimento:</label>
            <input type="date" id="dataNascimento" v-model="dataNascimento">
            <label for="email">E-mail:</label>
            <input type="email" id="email" v-model="email">
            <label for="senha">senha</label>
            <input type="text" id="senha" v-model="senha">
            <label for="Confirmação de senha">Confirmação de senha</label>
            <input type="text" id="Confirmação de senha" v-model="senha">

            <label for="rua">Rua:</label>
            <input type="text" id="rua" v-model="endereco.rua">
            <label for="numero">Número:</label>
            <input type="text" id="numero" v-model="endereco.numero">
            <label for="complemento">Complemento:</label>
            <input type="text" id="complemento" v-model="endereco.complemento">
            <label for="cidade">Cidade:</label>
            <input type="text" id="cidade" v-model="endereco.cidade">
            <label for="estado">Estado:</label>

        <select id="estado" v-model="endereco.estado">
            <option value="">Selecione um estado</option>
            <option value="AC">Acre</option>
            <option value="AL">Alagoas</option>
            <option value="AP">Amapá</option>
            <option value="AM">Amazonas</option>
            <option value="BA">Bahia</option>
            <option value="CE">Ceará</option>
            <option value="DF">Distrito Federal</option>
            <option value="ES">Espírito Santo</option>
            <option value="GO">Goiás</option>
            <option value="MA">Maranhão</option>
            <option value="MT">Mato Grosso</option>
            <option value="MS">Mato Grosso do Sul</option>
            <option value="MG">Minas Gerais</option>
            <option value="PA">Pará</option>
            <option value="PB">Paraíba</option>
            <option value="PR">Paraná</option>
            <option value="PE">Pernambuco</option>
            <option value="PI">Piauí</option>
            <option value="RJ">Rio de Janeiro</option>
            <option value="RN">Rio Grande do Norte</option>
            <option value="RS">Rio Grande do Sul</option>
            <option value="RO">Rondônia</option>
            <option value="RR">Roraima</option>
            <option value="SC">Santa Catarina</option>
            <option value="SP">São Paulo</option>
            <option value="SE">Sergipe</option>
            <option value="TO">Tocantins</option>
        </select>
            <button type="submit">Enviar</button>
        </form>
    
        <div v-if="formularioEnviado" class="div-informacoes">
      <h2>Informações preenchidas:</h2>
      <p><strong>Nome:</strong> {{ nome }}</p>
      <p><strong>Data de Nascimento:</strong> {{ dataNascimento }}</p>
      <p><strong>E-mail:</strong> {{ email }}</p>
      <p><strong>senha:</strong> {{ senha }}</p>
      <p><strong>Endereço:</strong> {{ endereco }}</p>
      
    </div>
      </div>
</template>

<script>export default {
    data() {
      return {
        nome: '',
        idade: '',
        email: '',
        endereco: {
        rua: '',
        numero: '',
        complemento: '',
        cidade: '',
        estado: '',
        }
      };
    },
    methods: {
        enviarFormulario() {
      
      this.formularioEnviado = true;
      }
    }
  };</script>

<style scoped>
.formulario {
  width: 400px;
  margin: 0 auto;
}

form{
  margin-top: 20px;
  padding: 10px;
  background-color: #f8f9fa;
  border: 1px solid #d6d8db;
  border-radius: 4px;
  
}

h2 {
  margin-top: 0;
}

.campo-formulario {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input,
select {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button[type="submit"] {
  width: 100%;
  padding: 10px;
  background-color: #007bff;
  color: #fff;
  font-size: 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.div-informacoes {
  margin-top: 20px;
  padding: 10px;
  background-color: #f8f9fa;
  border: 1px solid #d6d8db;
  border-radius: 4px;
}

.div-informacoes h2 {
  margin: 0 0 10px;
}

.div-informacoes p {
  margin: 0;
}
</style>