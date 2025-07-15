# 🚀 Módulo 3 – Aula 9: Montando o Layout Completo da Landing Page

## 🎯 Objetivos da Aula
- Criar uma landing page completa e funcional
- Aplicar todos os conceitos aprendidos até agora
- Desenvolver um projeto prático do início ao fim
- Implementar layout responsivo com Flexbox
- Organizar código de forma profissional

---

## 📋 Objetivo do Projeto

Criar uma **landing page** simples, moderna e responsiva para um produto ou serviço fictício.

### Estrutura da Landing Page
```
┌─────────────────────────────────┐
│           HEADER               │
│      Logo + Menu de Navegação  │
├─────────────────────────────────┤
│            HERO                │
│    Título + Texto + Botão      │
│         + Imagem               │
├─────────────────────────────────┤
│           SOBRE                │
│    Descrição do Produto        │
├─────────────────────────────────┤
│         VANTAGENS              │
│     3 Cards em Destaque        │
├─────────────────────────────────┤
│          CONTATO               │
│      Formulário de Contato     │
├─────────────────────────────────┤
│           FOOTER               │
│    Direitos + Links Sociais    │
└─────────────────────────────────┘
```

---

## 🏗️ Passo a Passo do Projeto

### ✅ Etapa 1: Estrutura HTML Básica

Crie um novo arquivo `index.html` com a seguinte estrutura:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Produto X - Landing Page</title>
  <link rel="stylesheet" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
</head>
<body>

  <header>
    <div class="container">
      <h1>Produto X</h1>
      <nav>
        <a href="#sobre">Sobre</a>
        <a href="#vantagens">Vantagens</a>
        <a href="#contato">Contato</a>
      </nav>
    </div>
  </header>

  <section class="hero">
    <div class="container">
      <div class="hero-content">
        <div class="hero-texto">
          <h2>Transforme sua experiência com o Produto X</h2>
          <p>Simples. Rápido. Inovador. Descubra como nossa solução pode revolucionar seu dia a dia.</p>
          <a href="#contato" class="botao">Quero saber mais</a>
        </div>
        <div class="hero-imagem">
          <img src="https://via.placeholder.com/400x300" alt="Imagem do Produto X">
        </div>
      </div>
    </div>
  </section>

  <section id="sobre" class="sobre">
    <div class="container">
      <h2>Sobre o Produto</h2>
      <p>O Produto X foi criado para facilitar sua vida com soluções modernas e acessíveis. Nossa missão é simplificar processos complexos e tornar sua experiência mais eficiente.</p>
    </div>
  </section>

  <section id="vantagens" class="vantagens">
    <div class="container">
      <h2>Nossas Vantagens</h2>
      <div class="cards">
        <div class="card">
          <h3>🚀 Velocidade</h3>
          <p>Resposta rápida e sem complicações. Processos otimizados para máxima eficiência.</p>
        </div>
        <div class="card">
          <h3>🎯 Facilidade</h3>
          <p>Interface intuitiva e direta ao ponto. Aprenda a usar em minutos.</p>
        </div>
        <div class="card">
          <h3>💬 Suporte</h3>
          <p>Estamos com você em cada passo. Suporte 24/7 sempre disponível.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="contato" class="contato">
    <div class="container">
      <h2>Entre em Contato</h2>
      <form>
        <div class="form-group">
          <label for="nome">Nome:</label>
          <input type="text" id="nome" name="nome" required>
        </div>
        
        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" id="email" name="email" required>
        </div>
        
        <div class="form-group">
          <label for="mensagem">Mensagem:</label>
          <textarea id="mensagem" name="mensagem" rows="4" required></textarea>
        </div>
        
        <button type="submit" class="botao">Enviar Mensagem</button>
      </form>
    </div>
  </section>

  <footer>
    <div class="container">
      <p>&copy; 2025 Produto X. Todos os direitos reservados.</p>
      <div class="social-links">
        <a href="#">Facebook</a>
        <a href="#">Twitter</a>
        <a href="#">LinkedIn</a>
      </div>
    </div>
  </footer>

</body>
</html>
```

---

### ✅ Etapa 2: Estrutura CSS Básica

Crie o arquivo `style.css` com a estrutura inicial:

```css
/* Reset e estilos globais */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Roboto', sans-serif;
  color: #333;
  line-height: 1.6;
  background-color: #f8f8f8;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Header */
header {
  background-color: #0066cc;
  color: white;
  padding: 20px 0;
  position: sticky;
  top: 0;
  z-index: 100;
}

header .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header h1 {
  font-size: 1.8rem;
  font-weight: 700;
}

nav a {
  margin: 0 15px;
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: opacity 0.3s ease;
}

nav a:hover {
  opacity: 0.8;
}

/* Hero Section */
.hero {
  padding: 80px 0;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.hero-content {
  display: flex;
  align-items: center;
  gap: 40px;
}

.hero-texto {
  flex: 1;
}

.hero-texto h2 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 20px;
}

.hero-texto p {
  font-size: 1.2rem;
  margin-bottom: 30px;
  opacity: 0.9;
}

.hero-imagem {
  flex: 1;
  text-align: center;
}

.hero-imagem img {
  max-width: 100%;
  border-radius: 10px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}

/* Botão */
.botao {
  display: inline-block;
  background-color: #ff6b35;
  color: white;
  padding: 15px 30px;
  text-decoration: none;
  border-radius: 5px;
  font-weight: 600;
  transition: all 0.3s ease;
  border: none;
  cursor: pointer;
  font-size: 1rem;
}

.botao:hover {
  background-color: #e55a2b;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

/* Seções gerais */
section {
  padding: 80px 0;
}

section h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 40px;
  color: #333;
}

/* Sobre */
.sobre {
  background-color: white;
  text-align: center;
}

.sobre p {
  font-size: 1.1rem;
  max-width: 800px;
  margin: 0 auto;
  color: #666;
}

/* Vantagens */
.vantagens {
  background-color: #f8f8f8;
}

.cards {
  display: flex;
  gap: 30px;
  justify-content: center;
}

.card {
  background-color: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  flex: 1;
  max-width: 350px;
  text-align: center;
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
}

.card h3 {
  font-size: 1.5rem;
  margin-bottom: 15px;
  color: #0066cc;
}

.card p {
  color: #666;
  line-height: 1.6;
}

/* Contato */
.contato {
  background-color: white;
}

form {
  max-width: 600px;
  margin: 0 auto;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 5px;
  font-weight: 600;
  color: #333;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 12px;
  border: 2px solid #ddd;
  border-radius: 5px;
  font-size: 1rem;
  transition: border-color 0.3s ease;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #0066cc;
}

/* Footer */
footer {
  background-color: #333;
  color: white;
  padding: 40px 0;
  text-align: center;
}

footer .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.social-links a {
  color: white;
  text-decoration: none;
  margin: 0 10px;
  transition: opacity 0.3s ease;
}

.social-links a:hover {
  opacity: 0.7;
}
```

---

## 📱 Responsividade

### Media Queries para Mobile

```css
/* Responsividade para tablets e mobile */
@media (max-width: 768px) {
  .container {
    padding: 0 15px;
  }
  
  /* Header mobile */
  header .container {
    flex-direction: column;
    gap: 15px;
  }
  
  nav a {
    margin: 0 10px;
  }
  
  /* Hero mobile */
  .hero-content {
    flex-direction: column;
    text-align: center;
    gap: 30px;
  }
  
  .hero-texto h2 {
    font-size: 2rem;
  }
  
  .hero-texto p {
    font-size: 1rem;
  }
  
  /* Cards mobile */
  .cards {
    flex-direction: column;
    align-items: center;
  }
  
  .card {
    max-width: 100%;
  }
  
  /* Footer mobile */
  footer .container {
    flex-direction: column;
    gap: 15px;
  }
}

/* Mobile pequeno */
@media (max-width: 480px) {
  .hero-texto h2 {
    font-size: 1.8rem;
  }
  
  section {
    padding: 60px 0;
  }
  
  section h2 {
    font-size: 2rem;
  }
}
```

---

## 📌 Missão para Aula 9

### ✅ Tarefas Obrigatórias:
1. **Copie e cole** o HTML acima no arquivo `index.html`
2. **Crie o arquivo** `style.css` com os estilos básicos
3. **Estilize pelo menos** o header, hero e footer
4. **Use Flexbox** para posicionar a imagem ao lado do texto na hero
5. **Adicione Media Queries** para alinhar tudo em coluna no celular

### 🎯 Objetivos de Aprendizado:
- ✅ **Estrutura HTML** semântica e organizada
- ✅ **CSS responsivo** com Flexbox
- ✅ **Media Queries** para diferentes dispositivos
- ✅ **Design moderno** e profissional
- ✅ **Código limpo** e bem organizado

### 💡 Dicas para o Projeto:
- **Teste em diferentes tamanhos** de tela
- **Use o DevTools** para verificar responsividade
- **Mantenha consistência** nas cores e fontes
- **Adicione transições** para melhor UX
- **Teste a navegação** entre seções

---

## 🔍 Próximos Passos

Após completar esta aula, você estará pronto para:
- 📚 **Aula 10**: Finalização e organização do projeto
- 🎨 **Melhorias visuais** e animações
- 🚀 **Otimizações** de performance
- 📱 **Testes** em dispositivos reais

---

*🎯 **Dica de Estudo**: Pratique muito com este projeto - é uma excelente base para portfólio!*