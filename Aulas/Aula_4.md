# 📚 Módulo 1 – Aula 4: Formulários em HTML

## 🎯 Objetivos da Aula
- Compreender o conceito e função dos formulários
- Aprender elementos básicos de formulário
- Criar formulários funcionais e acessíveis
- Entender métodos de envio (GET e POST)
- Implementar validação básica de campos

---

## 🧠 O que é um Formulário?

**Formulários** são elementos HTML usados para coletar dados do usuário e enviá-los para processamento (servidor, API, etc.).

### Estrutura Básica
```html
<form action="destino" method="método">
  <!-- campos do formulário aqui -->
</form>
```

### Atributos Principais

| Atributo | Função | Exemplo |
|----------|--------|---------|
| `action` | Para onde os dados serão enviados | `action="/processar.php"` |
| `method` | Como os dados serão enviados | `method="post"` |
| `name` | Identificador do formulário | `name="formulario-contato"` |

---

## 📋 Métodos de Envio

### GET vs POST

| Método | Características | Uso Recomendado |
|--------|----------------|-----------------|
| **GET** | Dados aparecem na URL | Buscas, filtros, navegação |
| **POST** | Dados enviados "escondidos" | Cadastros, login, dados sensíveis |

### Exemplos Práticos

```html
<!-- Busca (GET) -->
<form action="/buscar" method="get">
  <input type="text" name="q" placeholder="Digite sua busca...">
  <button type="submit">Buscar</button>
</form>

<!-- Cadastro (POST) -->
<form action="/cadastrar" method="post">
  <input type="text" name="nome" placeholder="Seu nome">
  <input type="email" name="email" placeholder="Seu email">
  <button type="submit">Cadastrar</button>
</form>
```

---

## 🧪 Elementos de Formulário

### Tags Principais

| Elemento | Função | Exemplo |
|----------|--------|---------|
| `<input>` | Campo genérico de entrada | `<input type="text">` |
| `<label>` | Texto que identifica o campo | `<label for="nome">Nome:</label>` |
| `<textarea>` | Área de texto maior | `<textarea rows="4"></textarea>` |
| `<select>` | Lista suspensa | `<select><option>Opção</option></select>` |
| `<button>` | Botão clicável | `<button type="submit">Enviar</button>` |
| `<fieldset>` | Agrupamento visual | `<fieldset><legend>Título</legend></fieldset>` |

---

## 📝 Tipos de Input

### Inputs de Texto

```html
<!-- Texto simples -->
<label for="nome">Nome completo:</label>
<input type="text" id="nome" name="nome" placeholder="Digite seu nome">

<!-- Email -->
<label for="email">Email:</label>
<input type="email" id="email" name="email" required>

<!-- Senha -->
<label for="senha">Senha:</label>
<input type="password" id="senha" name="senha" minlength="6">

<!-- Número -->
<label for="idade">Idade:</label>
<input type="number" id="idade" name="idade" min="0" max="120">

<!-- Telefone -->
<label for="telefone">Telefone:</label>
<input type="tel" id="telefone" name="telefone" pattern="[0-9]{2}-[0-9]{5}-[0-9]{4}">
```

### Inputs Especiais

```html
<!-- Data -->
<label for="nascimento">Data de nascimento:</label>
<input type="date" id="nascimento" name="nascimento">

<!-- Hora -->
<label for="horario">Horário preferido:</label>
<input type="time" id="horario" name="horario">

<!-- Cor -->
<label for="cor-favorita">Cor favorita:</label>
<input type="color" id="cor-favorita" name="cor-favorita">

<!-- Arquivo -->
<label for="foto">Sua foto:</label>
<input type="file" id="foto" name="foto" accept="image/*">
```

### Inputs de Seleção

```html
<!-- Checkbox -->
<label for="newsletter">
  <input type="checkbox" id="newsletter" name="newsletter">
  Quero receber newsletter
</label>

<!-- Radio buttons -->
<fieldset>
  <legend>Gênero:</legend>
  <label for="masculino">
    <input type="radio" id="masculino" name="genero" value="masculino">
    Masculino
  </label>
  <label for="feminino">
    <input type="radio" id="feminino" name="genero" value="feminino">
    Feminino
  </label>
</fieldset>
```

---

## 📄 Área de Texto

### Textarea Básico
```html
<label for="bio">Sobre você:</label>
<textarea id="bio" name="bio" rows="4" cols="50" placeholder="Conte um pouco sobre você..."></textarea>
```

### Atributos do Textarea
| Atributo | Função |
|----------|--------|
| `rows` | Número de linhas visíveis |
| `cols` | Número de colunas |
| `placeholder` | Texto de exemplo |
| `maxlength` | Máximo de caracteres |

---

## 📋 Lista Suspensa

### Select Simples
```html
<label for="linguagem">Linguagem favorita:</label>
<select id="linguagem" name="linguagem">
  <option value="">Selecione uma opção</option>
  <option value="html">HTML</option>
  <option value="css">CSS</option>
  <option value="javascript">JavaScript</option>
  <option value="python">Python</option>
</select>
```

### Select com Grupos
```html
<label for="categoria">Categoria:</label>
<select id="categoria" name="categoria">
  <optgroup label="Front-end">
    <option value="html">HTML</option>
    <option value="css">CSS</option>
    <option value="javascript">JavaScript</option>
  </optgroup>
  <optgroup label="Back-end">
    <option value="python">Python</option>
    <option value="java">Java</option>
    <option value="php">PHP</option>
  </optgroup>
</select>
```

---

## 🔘 Botões

### Tipos de Botão
```html
<!-- Botão de envio -->
<button type="submit">Enviar Formulário</button>

<!-- Botão de reset -->
<button type="reset">Limpar Campos</button>

<!-- Botão genérico -->
<button type="button" onclick="minhaFuncao()">Clique aqui</button>

<!-- Input como botão -->
<input type="submit" value="Enviar">
<input type="reset" value="Limpar">
```

---

## ✅ Exercício Prático

### 📝 Tarefa
Crie um formulário de contato em seu `index.html` com os seguintes campos:

1. **Nome completo** (input texto)
2. **Email** (input email)
3. **Mensagem** (textarea)
4. **Linguagem favorita** (select com 3+ opções)
5. **Botão de envio**

### 🎯 Estrutura Esperada

```html
<section id="contato">
  <h2>Fale comigo</h2>
  
  <form action="#" method="post">
    <fieldset>
      <legend>Informações de Contato</legend>
      
      <div>
        <label for="nome">Nome completo:</label>
        <input type="text" id="nome" name="nome" required>
      </div>
      
      <div>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
      </div>
      
      <div>
        <label for="mensagem">Mensagem:</label>
        <textarea id="mensagem" name="mensagem" rows="4" placeholder="Digite sua mensagem..."></textarea>
      </div>
      
      <div>
        <label for="linguagem">Linguagem favorita:</label>
        <select id="linguagem" name="linguagem">
          <option value="">Selecione uma opção</option>
          <option value="html">HTML</option>
          <option value="css">CSS</option>
          <option value="javascript">JavaScript</option>
          <option value="python">Python</option>
        </select>
      </div>
      
      <button type="submit">Enviar Mensagem</button>
    </fieldset>
  </form>
</section>
```

### 💡 Dicas para o Exercício
- **Use `label for="id"`** combinando com `id` do campo para melhorar acessibilidade
- **Adicione `required`** nos campos obrigatórios
- **Use `placeholder`** para dar dicas ao usuário
- **Organize com `fieldset`** para agrupar campos relacionados
- **Teste o formulário** abrindo no navegador

---

## 🛠️ Validação e Boas Práticas

### Validação HTML5
```html
<!-- Campos obrigatórios -->
<input type="text" required>

<!-- Validação de email -->
<input type="email" required>

<!-- Comprimento mínimo -->
<input type="password" minlength="6">

<!-- Padrão específico -->
<input type="tel" pattern="[0-9]{2}-[0-9]{5}-[0-9]{4}">
```

### Boas Práticas
- ✅ **Sempre use `<label>`** para identificar campos
- ✅ **Adicione `required`** em campos obrigatórios
- ✅ **Use `placeholder`** para orientar o usuário
- ✅ **Agrupe campos** com `<fieldset>` e `<legend>`
- ✅ **Teste a acessibilidade** com leitores de tela

### Checklist de Validação
- [ ] Todos os campos têm `<label>`
- [ ] Campos obrigatórios têm `required`
- [ ] Formulário tem `action` e `method`
- [ ] Botão de envio funciona
- [ ] Campos têm `id` e `name` apropriados

---

## 🔍 Próximos Passos
- ✅ Dominar formulários HTML básicos
- 📚 Aprender sobre tabelas HTML
- 🎨 Introdução ao CSS na próxima aula
- 🚀 Criar formulários mais complexos

---

## 📚 Recursos Adicionais

### Documentação
- [MDN - Formulários HTML](https://developer.mozilla.org/pt-BR/docs/Learn/Forms)
- [W3Schools - HTML Forms](https://www.w3schools.com/html/html_forms.asp)

### Ferramentas
- [HTML Form Validator](https://www.freeformatter.com/html-validator.html)
- [Formspree](https://formspree.io/) - Processamento de formulários

---

*🎯 **Dica de Estudo**: Pratique criando diferentes tipos de formulários para fixar cada elemento!*