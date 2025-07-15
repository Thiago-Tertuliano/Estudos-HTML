# 📚 Módulo 1 – Aula 3: Semântica HTML e Estrutura de Página

## 🎯 Objetivos da Aula
- Compreender o conceito de semântica HTML
- Aprender tags semânticas e suas funções
- Estruturar páginas de forma semântica
- Melhorar acessibilidade e SEO
- Organizar código de forma profissional

---

## 🧠 O que é Semântica HTML?

**Semântica** é sobre dar significado às partes da sua página. Em vez de usar apenas `<div>` para tudo, usamos tags com nomes claros e específicos.

### Por que usar Semântica?

| Benefício | Descrição |
|-----------|-----------|
| **Acessibilidade** | Leitores de tela entendem melhor a estrutura |
| **SEO** | Motores de busca compreendem o conteúdo |
| **Organização** | Código mais limpo e legível |
| **Manutenção** | Facilita futuras modificações |

### Comparação: Semântico vs Não-Semântico

```html
<!-- ❌ Não-semântico -->
<div class="header">
  <div class="nav">
    <div class="menu-item">Home</div>
  </div>
</div>

<!-- ✅ Semântico -->
<header>
  <nav>
    <a href="#home">Home</a>
  </nav>
</header>
```

---

## 🏗️ Estrutura Semântica de uma Página

### Template Completo
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu Portfólio</title>
</head>
<body>
  <header>
    <!-- Logo, título, navegação principal -->
    <h1>Meu Nome</h1>
    <nav>
      <a href="#sobre">Sobre</a>
      <a href="#projetos">Projetos</a>
      <a href="#contato">Contato</a>
    </nav>
  </header>

  <main>
    <!-- Conteúdo principal da página -->
    <section id="sobre">
      <h2>Sobre mim</h2>
      <p>Descrição sobre você...</p>
    </section>

    <section id="projetos">
      <h2>Meus Projetos</h2>
      <article>
        <h3>Projeto 1</h3>
        <p>Descrição do projeto...</p>
      </article>
    </section>
  </main>

  <aside>
    <!-- Conteúdo lateral -->
    <h3>Links Úteis</h3>
    <ul>
      <li><a href="#">GitHub</a></li>
      <li><a href="#">LinkedIn</a></li>
    </ul>
  </aside>

  <footer>
    <!-- Informações finais -->
    <p>&copy; 2025 Seu Nome. Todos os direitos reservados.</p>
  </footer>
</body>
</html>
```

---

## 📋 Principais Tags Semânticas

### Tags de Estrutura Principal

| Tag | Função | Exemplo de Uso |
|-----|--------|----------------|
| `<header>` | Cabeçalho da página ou seção | Logo, título, navegação principal |
| `<nav>` | Navegação principal ou secundária | Menu, links de navegação |
| `<main>` | Conteúdo principal e único da página | Conteúdo central da página |
| `<section>` | Bloco temático de conteúdo | Seções como "Sobre", "Projetos" |
| `<article>` | Conteúdo independente | Post de blog, notícia, produto |
| `<aside>` | Conteúdo lateral ou complementar | Sidebar, links relacionados |
| `<footer>` | Rodapé da página ou seção | Contato, copyright, links finais |

### Tags de Conteúdo

| Tag | Função | Exemplo de Uso |
|-----|--------|----------------|
| `<h1>` a `<h6>` | Títulos hierárquicos | Estrutura de títulos |
| `<p>` | Parágrafos | Texto corrido |
| `<ul>`, `<ol>`, `<li>` | Listas | Navegação, itens |
| `<a>` | Links | Navegação, referências |
| `<img>` | Imagens | Conteúdo visual |

### Exemplo de Estrutura Semântica
```html
<header>
  <h1>Lucas Moura</h1>
  <nav>
    <a href="#sobre">Sobre</a>
    <a href="#skills">Skills</a>
    <a href="#contato">Contato</a>
  </nav>
</header>

<main>
  <section id="sobre">
    <h2>Sobre mim</h2>
    <p>Sou desenvolvedor web apaixonado por criar experiências digitais incríveis.</p>
  </section>

  <section id="skills">
    <h2>Minhas Habilidades</h2>
    <ul>
      <li>HTML5</li>
      <li>CSS3</li>
      <li>JavaScript</li>
    </ul>
  </section>
</main>

<footer>
  <p>&copy; 2025 Lucas Moura. Todos os direitos reservados.</p>
</footer>
```

---

## ✅ Exercício Prático

### 📝 Tarefa
Reestruture seu arquivo `index.html` usando semântica HTML:

1. **Envolva o conteúdo** com tags semânticas apropriadas
2. **Organize em seções** lógicas
3. **Adicione navegação** no header
4. **Crie um footer** com informações de contato

### 🎯 Estrutura Esperada

```html
<body>
  <header>
    <h1>Seu Nome</h1>
    <nav>
      <a href="#sobre">Sobre</a>
      <a href="#skills">Skills</a>
      <a href="#metas">Metas</a>
    </nav>
  </header>

  <main>
    <section id="sobre">
      <h2>Sobre mim</h2>
      <p>Seu parágrafo sobre você...</p>
    </section>

    <section id="skills">
      <h2>Linguagens que estou aprendendo</h2>
      <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
      </ul>
    </section>

    <section id="metas">
      <h2>Minhas metas</h2>
      <ol>
        <li>Primeira meta</li>
        <li>Segunda meta</li>
        <li>Terceira meta</li>
      </ol>
    </section>

    <section id="recursos">
      <h2>Links e Imagem</h2>
      <a href="https://developer.mozilla.org/" target="_blank">MDN</a>
      <img src="https://via.placeholder.com/300x200" alt="Imagem de exemplo">
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Seu Nome. Todos os direitos reservados.</p>
    <p>Contato: seu@email.com</p>
  </footer>
</body>
```

### 💡 Dicas para o Exercício
- **Evite usar `<div>`** por enquanto - foque em tags semânticas
- **Revise a indentação** para manter o código organizado
- **Use IDs nas seções** para navegação interna
- **Mantenha a hierarquia** de títulos (h1, h2, h3)

---

## 🛠️ Validação e Boas Práticas

### Validador HTML
- Use o [W3C Validator](https://validator.w3.org/) para verificar seu código
- Cole seu HTML e verifique se não há erros de estrutura

### Boas Práticas
- ✅ **Use apenas um `<h1>`** por página
- ✅ **Mantenha hierarquia** de títulos (h1 → h2 → h3)
- ✅ **Adicione `alt`** em todas as imagens
- ✅ **Use `target="_blank"`** para links externos
- ✅ **Organize o código** com indentação consistente

### Checklist de Validação
- [ ] Estrutura HTML válida
- [ ] Tags semânticas apropriadas
- [ ] Hierarquia de títulos correta
- [ ] Links funcionando
- [ ] Imagens com alt
- [ ] Código bem indentado

---

## 🔍 Próximos Passos
- ✅ Dominar estrutura semântica HTML
- 📚 Aprender sobre formulários e tabelas
- 🎨 Introdução ao CSS na próxima aula
- 🚀 Criar layouts mais complexos

---

## 📚 Recursos Adicionais

### Documentação
- [MDN - HTML Semântico](https://developer.mozilla.org/pt-BR/docs/Glossary/Semantics)
- [W3Schools - HTML5 Semantic Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)

### Ferramentas
- [W3C Validator](https://validator.w3.org/) - Validação de HTML
- [HTML5 Outliner](https://gsnedders.html5.org/outliner/) - Estrutura de títulos

---

*🎯 **Dica de Estudo**: Pratique criando diferentes layouts semânticos para fixar cada tag!*