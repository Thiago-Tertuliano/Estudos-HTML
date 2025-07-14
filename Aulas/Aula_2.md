# 📚 Módulo 1 – Aula 2: Elementos Básicos do HTML

## 🎯 Objetivos da Aula
- Aprender tags de texto e formatação
- Trabalhar com listas ordenadas e não ordenadas
- Criar links e navegação
- Inserir e configurar imagens
- Enriquecer páginas HTML com conteúdo dinâmico

---

## 📝 Tags de Texto e Formatação

### Títulos Hierárquicos
```html
<h1>Título Principal</h1>
<h2>Subtítulo</h2>
<h3>Seção</h3>
<h4>Subseção</h4>
<h5>Item menor</h5>
<h6>Item menor ainda</h6>
```

### Parágrafos e Formatação
```html
<p>Este é um parágrafo normal.</p>
<p>Texto com <strong>negrito</strong> para destaque importante.</p>
<p>Texto com <em>itálico</em> para ênfase.</p>
```

### Exemplo Prático
```html
<h2>Sobre mim</h2>
<p>Sou um entusiasta de tecnologia e gosto de <strong>desenvolvimento web</strong>.</p>
<p>Estou <em>muito animado</em> para aprender HTML e CSS!</p>
```

---

## 📋 Trabalhando com Listas

### Lista Não Ordenada (Bullets)
```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
  <li>React</li>
</ul>
```

### Lista Ordenada (Números)
```html
<ol>
  <li>Aprender HTML</li>
  <li>Estudar CSS</li>
  <li>Praticar JavaScript</li>
  <li>Criar projetos práticos</li>
</ol>
```

### Listas Aninhadas
```html
<ul>
  <li>Front-end
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
    </ul>
  </li>
  <li>Back-end
    <ul>
      <li>Node.js</li>
      <li>Python</li>
    </ul>
  </li>
</ul>
```

---

## 🔗 Criando Links (Âncoras)

### Estrutura Básica
```html
<a href="URL_DO_LINK">Texto do link</a>
```

### Exemplos Práticos
```html
<!-- Link externo que abre em nova aba -->
<a href="https://developer.mozilla.org/pt-BR/" target="_blank">
  Documentação do MDN
</a>

<!-- Link interno para seção da página -->
<a href="#sobre-mim">Ir para Sobre Mim</a>

<!-- Link para email -->
<a href="mailto:seu@email.com">Enviar email</a>

<!-- Link para telefone -->
<a href="tel:+5511999999999">Ligar agora</a>
```

### Atributos Importantes
| Atributo | Função |
|----------|--------|
| `href` | URL de destino do link |
| `target="_blank"` | Abre em nova aba |
| `title` | Tooltip ao passar o mouse |
| `rel="noopener"` | Segurança para links externos |

---

## 🖼️ Inserindo Imagens

### Estrutura Básica
```html
<img src="caminho-da-imagem.jpg" alt="Descrição da imagem">
```

### Exemplos Práticos
```html
<!-- Imagem local -->
<img src="imagens/foto.jpg" alt="Minha foto de perfil">

<!-- Imagem da internet -->
<img src="https://via.placeholder.com/300x200" alt="Imagem de exemplo">

<!-- Imagem com dimensões -->
<img src="logo.png" alt="Logo da empresa" width="200" height="100">

<!-- Imagem responsiva -->
<img src="banner.jpg" alt="Banner principal" style="max-width: 100%; height: auto;">
```

### Atributos Importantes
| Atributo | Função |
|----------|--------|
| `src` | Caminho da imagem |
| `alt` | Texto alternativo (acessibilidade) |
| `width` | Largura da imagem |
| `height` | Altura da imagem |
| `title` | Tooltip ao passar o mouse |

---

## ✅ Exercício Prático

### 📝 Tarefa
Enriqueça seu arquivo `index.html` adicionando:

1. **Seção "Linguagens que estou aprendendo"**
   - Subtítulo `<h2>`
   - Lista não ordenada com 3+ linguagens

2. **Seção "Minhas metas"**
   - Subtítulo `<h2>`
   - Lista ordenada com 3 objetivos

3. **Recursos externos**
   - Link para site de estudo (YouTube, Alura, MDN, etc.)
   - Imagem de sua escolha

### 🎯 Exemplo de Estrutura Esperada

```html
<h2>Linguagens que estou aprendendo</h2>
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
  <li>React</li>
</ul>

<h2>Minhas metas</h2>
<ol>
  <li>Fazer meu primeiro site completo</li>
  <li>Criar um portfólio profissional</li>
  <li>Conseguir meu primeiro projeto freelance</li>
</ol>

<h2>Recursos de estudo</h2>
<p>Gosto de estudar no <a href="https://developer.mozilla.org/" target="_blank">MDN</a>.</p>
<img src="https://via.placeholder.com/300x200" alt="Imagem de exemplo">
```

### 💡 Dicas para o Exercício
- **Imagens gratuitas**: Use [Unsplash](https://unsplash.com) ou [Pexels](https://pexels.com)
- **Placeholder**: Para testes, use `https://via.placeholder.com/300x200`
- **Links externos**: Sempre use `target="_blank"` para abrir em nova aba
- **Acessibilidade**: Sempre adicione `alt` nas imagens

---

## 🔍 Próximos Passos
- ✅ Dominar elementos básicos de texto e formatação
- 📚 Aprender sobre tabelas e formulários
- 🎨 Introdução ao CSS na próxima aula
- 🚀 Criar páginas mais complexas e interativas

---

## 📚 Recursos Adicionais

### Sites para Imagens Gratuitas
- [Unsplash](https://unsplash.com) - Fotos de alta qualidade
- [Pexels](https://pexels.com) - Banco de imagens gratuito
- [Pixabay](https://pixabay.com) - Imagens e ilustrações

### Documentação
- [MDN Web Docs](https://developer.mozilla.org/pt-BR/) - Referência oficial
- [W3Schools](https://www.w3schools.com/html/) - Tutoriais práticos

---

*🎯 **Dica de Estudo**: Pratique criando diferentes tipos de conteúdo para fixar cada elemento!*