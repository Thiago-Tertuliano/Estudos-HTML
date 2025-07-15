# 🎨 Módulo 2 – Aula 5: Introdução ao CSS

## 🎯 Objetivos da Aula
- Compreender o que é CSS e sua função
- Aprender as três formas de aplicar CSS
- Dominar seletores CSS básicos
- Criar arquivos CSS externos
- Aplicar estilos básicos em elementos HTML

---

## 🧠 O que é CSS?

**CSS** (Cascading Style Sheets) é a linguagem usada para estilizar o HTML — controlar cores, fontes, tamanhos, posicionamento e aparência visual de tudo.

### Funções do CSS
- 🎨 **Estilização visual** (cores, fontes, tamanhos)
- 📐 **Layout e posicionamento** (margens, padding, flexbox)
- 🎭 **Animações e transições** (efeitos visuais)
- 📱 **Responsividade** (adaptação a diferentes telas)

---

## 📋 Três Formas de Usar CSS

### Comparação dos Métodos

| Método | Exemplo | Vantagens | Desvantagens | Uso Recomendado |
|--------|---------|-----------|---------------|-----------------|
| **Inline** | `<p style="color:red;">Oi</p>` | Rápido para testes | Difícil manutenção | ❌ Não recomendado |
| **Interno** | `<style>` no `<head>` | Fácil para testes | Não reutilizável | ⚠️ Apenas testes |
| **Externo** | Arquivo `.css` separado | Manutenível, reutilizável | Requer arquivo extra | ✅ Recomendado |

### Exemplos Práticos

```html
<!-- ❌ Inline (não recomendado) -->
<p style="color: red; font-size: 18px;">Texto vermelho</p>

<!-- ⚠️ Interno (apenas testes) -->
<head>
  <style>
    p {
      color: blue;
      font-size: 16px;
    }
  </style>
</head>

<!-- ✅ Externo (recomendado) -->
<head>
  <link rel="stylesheet" href="style.css">
</head>
```

---

## 📁 Como Criar CSS Externo

### Passo a Passo

1. **Crie um arquivo** chamado `style.css`
2. **Conecte no HTML** dentro da tag `<head>`
3. **Escreva seus estilos** no arquivo CSS

### Estrutura do Projeto
```
seu-projeto/
├── index.html
├── style.css
└── imagens/
```

### Conectando CSS ao HTML
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu Site</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- conteúdo aqui -->
</body>
</html>
```

---

## ✏️ Conceito-Chave: Seletores CSS

### Sintaxe Básica
```css
seletor {
  propriedade: valor;
}
```

### Tipos de Seletores

#### 1. Seletores de Tag
```css
/* Aplica em todas as tags <p> */
p {
  color: blue;
  font-size: 16px;
}

/* Aplica em todas as tags <h1> */
h1 {
  color: red;
  font-size: 24px;
}
```

#### 2. Seletores de Classe
```css
/* Aplica em elementos com class="destaque" */
.destaque {
  background-color: yellow;
  padding: 10px;
}

/* Aplica em elementos com class="titulo" */
.titulo {
  color: #0066cc;
  font-size: 28px;
}
```

#### 3. Seletores de ID
```css
/* Aplica no elemento com id="principal" */
#principal {
  text-align: center;
  background-color: #f0f0f0;
}
```

#### 4. Seletores Múltiplos
```css
/* Aplica em h1 E h2 */
h1, h2 {
  color: #0066cc;
  font-family: Arial, sans-serif;
}

/* Aplica em elementos com classes específicas */
.titulo, .subtitulo {
  margin-bottom: 20px;
}
```

---

## 📌 Principais Propriedades CSS

### Propriedades de Texto

| Propriedade | Função | Exemplo |
|-------------|--------|---------|
| `color` | Cor do texto | `color: #333;` |
| `font-size` | Tamanho da fonte | `font-size: 16px;` |
| `font-family` | Tipo da fonte | `font-family: Arial, sans-serif;` |
| `text-align` | Alinhamento do texto | `text-align: center;` |
| `line-height` | Altura da linha | `line-height: 1.5;` |

### Propriedades de Fundo e Borda

| Propriedade | Função | Exemplo |
|-------------|--------|---------|
| `background-color` | Cor de fundo | `background-color: #f0f0f0;` |
| `border` | Borda | `border: 1px solid black;` |
| `border-radius` | Bordas arredondadas | `border-radius: 8px;` |

### Propriedades de Espaçamento

| Propriedade | Função | Exemplo |
|-------------|--------|---------|
| `margin` | Espaço externo | `margin: 10px;` |
| `padding` | Espaço interno | `padding: 15px;` |

### Exemplos Práticos

```css
/* Estilo para o corpo da página */
body {
  background-color: #f2f2f2;
  font-family: Arial, sans-serif;
  color: #333;
  margin: 0;
  padding: 20px;
}

/* Estilo para títulos */
h1, h2 {
  color: #0066cc;
  font-size: 24px;
  margin-bottom: 15px;
}

/* Estilo para parágrafos */
p {
  line-height: 1.6;
  margin-bottom: 10px;
}

/* Estilo para listas */
ul, ol {
  padding-left: 20px;
  margin-bottom: 15px;
}

/* Estilo para links */
a {
  color: #cc0000;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

/* Estilo para imagens */
img {
  max-width: 100%;
  border-radius: 8px;
  margin: 10px 0;
}
```

---

## ✅ Exercício Prático

### 📝 Tarefa
Crie o arquivo `style.css` e conecte ao seu HTML. Aplique os seguintes estilos:

### 🎯 Estilos Básicos

```css
/* Estilos gerais */
body {
  background-color: #f2f2f2;
  font-family: sans-serif;
  color: #333;
  margin: 0;
  padding: 20px;
}

/* Títulos */
h1, h2 {
  color: #0066cc;
}

/* Parágrafos */
p {
  line-height: 1.5;
}

/* Listas */
ul, ol {
  padding-left: 20px;
}

/* Links */
a {
  color: #cc0000;
  text-decoration: none;
}

/* Imagens */
img {
  max-width: 100%;
  border-radius: 8px;
}
```

### 🎨 Classe Personalizada

```css
/* Crie uma classe personalizada */
.destaque {
  background-color: yellow;
  padding: 10px;
  border-left: 4px solid orange;
  margin: 10px 0;
}
```

### 📝 Aplicando no HTML

```html
<!-- Adicione a classe em um elemento -->
<p class="destaque">Esse parágrafo está em destaque!</p>

<!-- Ou aplique em outros elementos -->
<div class="destaque">
  <h3>Seção em destaque</h3>
  <p>Conteúdo importante aqui.</p>
</div>
```

### 💡 Dicas para o Exercício
- **Teste mudando cores** do fundo e texto
- **Experimente diferentes fontes** (Arial, Verdana, Georgia)
- **Ajuste tamanhos** de fonte e espaçamentos
- **Teste bordas arredondadas** nas imagens
- **Crie suas próprias classes** para elementos específicos

---

## 🧪 Testes Rápidos

### Experimente estas modificações:

```css
/* Teste 1: Mude a cor do fundo */
body {
  background-color: #e8f4f8; /* Azul claro */
}

/* Teste 2: Mude o tamanho dos títulos */
h1 {
  font-size: 32px;
}

h2 {
  font-size: 24px;
}

/* Teste 3: Adicione bordas nas imagens */
img {
  border: 3px solid #0066cc;
  border-radius: 12px;
}

/* Teste 4: Crie um estilo para links */
a {
  color: #0066cc;
  font-weight: bold;
}

a:hover {
  color: #cc0000;
}
```

---

## 🔍 Próximos Passos
- ✅ Dominar seletores CSS básicos
- 📚 Aprender sobre box model e layout
- 🎨 Explorar flexbox e grid
- 🚀 Criar layouts responsivos

---

## 📚 Recursos Adicionais

### Documentação
- [MDN - CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
- [W3Schools - CSS Tutorial](https://www.w3schools.com/css/)

### Ferramentas
- [CSS Validator](https://jigsaw.w3.org/css-validator/) - Validação de CSS
- [Color Picker](https://www.w3schools.com/colors/colors_picker.asp) - Seletor de cores

### Paletas de Cores
- [Coolors](https://coolors.co/) - Gerador de paletas
- [Adobe Color](https://color.adobe.com/) - Ferramenta de cores

---

*🎯 **Dica de Estudo**: Experimente muito com cores e fontes para desenvolver seu senso visual!*

