# 🎨 Módulo 2 – Aula 6: Cores, Fontes, Espaçamento e Box Model

## 🎯 Objetivos da Aula
- Dominar diferentes formas de aplicar cores em CSS
- Trabalhar com fontes web e Google Fonts
- Compreender o Box Model completo
- Aprender unidades de medida CSS
- Criar layouts com espaçamento adequado

---

## 🎨 Cores em CSS

### Formas de Definir Cores

#### 1. Palavras-chave
```css
body {
  background-color: red;
  color: black;
  border-color: blue;
}
```

#### 2. Hexadecimal (#RRGGBB)
```css
body {
  background-color: #fafafa;  /* Cinza claro */
  color: #222;                /* Cinza escuro */
  border-color: #0066cc;      /* Azul */
}
```

#### 3. RGB e RGBA
```css
body {
  background-color: rgb(255, 255, 255);  /* Branco */
  color: rgb(34, 34, 34);                /* Cinza escuro */
  border-color: rgba(0, 102, 204, 0.5); /* Azul com transparência */
}
```

### Paleta de Cores Comum

| Cor | Hexadecimal | RGB | Uso |
|-----|-------------|-----|-----|
| Branco | `#ffffff` | `rgb(255, 255, 255)` | Fundos claros |
| Preto | `#000000` | `rgb(0, 0, 0)` | Texto principal |
| Cinza claro | `#f5f5f5` | `rgb(245, 245, 245)` | Fundos secundários |
| Azul | `#0066cc` | `rgb(0, 102, 204)` | Links e destaque |
| Vermelho | `#cc0000` | `rgb(204, 0, 0)` | Erros e alertas |

### Exemplo Prático
```css
body {
  background-color: #fafafa;
  color: #222;
}

h1 {
  color: #0066cc;
}

.destaque {
  background-color: rgba(255, 255, 0, 0.3);
  color: #333;
}
```

---

## 🔤 Fontes em CSS

### Fontes do Sistema
```css
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
}
```

### Propriedades de Fonte

| Propriedade | Função | Exemplo |
|-------------|--------|---------|
| `font-family` | Tipo da fonte | `Arial, sans-serif` |
| `font-size` | Tamanho da fonte | `16px`, `1.2em` |
| `font-weight` | Peso da fonte | `normal`, `bold`, `400` |
| `font-style` | Estilo da fonte | `normal`, `italic` |
| `line-height` | Altura da linha | `1.5`, `24px` |

### Google Fonts

#### 1. Importar no HTML
```html
<head>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
</head>
```

#### 2. Usar no CSS
```css
body {
  font-family: 'Roboto', sans-serif;
  font-weight: 400;
}

h1 {
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  font-size: 2.5rem;
}
```

### Fontes Populares do Google Fonts

| Fonte | Import | CSS |
|-------|--------|-----|
| Roboto | `family=Roboto` | `'Roboto', sans-serif` |
| Open Sans | `family=Open+Sans` | `'Open Sans', sans-serif` |
| Lato | `family=Lato` | `'Lato', sans-serif` |
| Poppins | `family=Poppins` | `'Poppins', sans-serif` |

---

## 📦 Box Model (Modelo de Caixa)

### Estrutura do Box Model

```
┌─────────────────────────────────────────┐
│              MARGIN                    │
│  ┌─────────────────────────────────┐   │
│  │            BORDER              │   │
│  │  ┌─────────────────────────┐   │   │
│  │  │        PADDING         │   │   │
│  │  │  ┌─────────────────┐   │   │   │
│  │  │  │    CONTEÚDO    │   │   │   │
│  │  │  └─────────────────┘   │   │   │
│  │  └─────────────────────────┘   │   │
│  └─────────────────────────────────┘   │
└─────────────────────────────────────────┘
```

### Propriedades do Box Model

| Propriedade | Função | Exemplo |
|-------------|--------|---------|
| `margin` | Espaço externo | `margin: 20px;` |
| `padding` | Espaço interno | `padding: 15px;` |
| `border` | Borda | `border: 1px solid black;` |
| `width` | Largura | `width: 300px;` |
| `height` | Altura | `height: 200px;` |

### Exemplo Prático
```css
.card {
  background-color: white;
  padding: 20px;
  margin: 20px;
  border: 2px solid #ddd;
  border-radius: 8px;
  width: 300px;
  height: auto;
}
```

---

## 🔢 Unidades de Medida CSS

### Unidades Absolutas

| Unidade | Descrição | Exemplo |
|---------|-----------|---------|
| `px` | Pixels (fixo) | `16px` |
| `pt` | Pontos | `12pt` |
| `in` | Polegadas | `1in` |
| `cm` | Centímetros | `2.54cm` |

### Unidades Relativas

| Unidade | Descrição | Exemplo |
|---------|-----------|---------|
| `%` | Porcentagem do elemento pai | `50%` |
| `em` | Relativo ao elemento pai | `1.5em` |
| `rem` | Relativo ao `<html>` | `1.2rem` |
| `vh` | Viewport height | `50vh` |
| `vw` | Viewport width | `100vw` |

### Exemplos Práticos
```css
/* Tamanhos responsivos */
.container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
}

/* Texto responsivo */
h1 {
  font-size: 2.5rem;  /* 40px se html = 16px */
}

p {
  font-size: 1.1em;   /* Relativo ao pai */
  line-height: 1.6;
}

/* Altura da viewport */
.hero {
  height: 100vh;
  width: 100vw;
}
```

---

## ✅ Exercício Prático

### 📝 Tarefa
Crie uma div com a classe `card` contendo:
- Um título
- Um parágrafo
- Um link

### 🎯 Estrutura HTML

```html
<div class="card">
  <h2>Meu Card</h2>
  <p>Esse é um exemplo de caixa com padding, borda e margem.</p>
  <a href="#">Saiba mais</a>
</div>
```

### 🎨 Estilos CSS

```css
.card {
  background-color: #ffffff;
  padding: 20px;
  margin: 20px auto;
  border: 1px solid #ccc;
  border-radius: 8px;
  width: 300px;
  font-family: 'Roboto', sans-serif;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.card h2 {
  color: #0066cc;
  margin-bottom: 15px;
  font-size: 1.5rem;
}

.card p {
  color: #333;
  line-height: 1.6;
  margin-bottom: 15px;
}

.card a {
  color: #cc0000;
  text-decoration: none;
  font-weight: bold;
}

.card a:hover {
  text-decoration: underline;
}
```

### 💡 Dicas para o Exercício
- **Teste removendo o padding** e veja como o conteúdo fica colado na borda
- **Experimente margin: 0** para ver o comportamento sem espaçamento externo
- **Aumente a border** para ver como afeta o tamanho total
- **Teste diferentes cores** de fundo e texto
- **Experimente fontes do Google Fonts**

---

## 🧪 Testes e Experimentos

### Teste 1: Box Model
```css
/* Remova o padding */
.card {
  padding: 0;
}

/* Remova a margin */
.card {
  margin: 0;
}

/* Aumente a border */
.card {
  border: 5px solid #0066cc;
}
```

### Teste 2: Cores
```css
/* Mude as cores */
.card {
  background-color: #f0f8ff;  /* Azul claro */
  color: #2c3e50;             /* Azul escuro */
}

.card h2 {
  color: #e74c3c;             /* Vermelho */
}
```

### Teste 3: Fontes
```css
/* Importe uma nova fonte */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

.card {
  font-family: 'Poppins', sans-serif;
}
```

---

## 🔍 Próximos Passos
- ✅ Dominar Box Model e espaçamento
- 📚 Aprender sobre Flexbox e Grid
- 🎨 Explorar layouts responsivos
- 🚀 Criar designs mais complexos

---

## 📚 Recursos Adicionais

### Ferramentas de Cores
- [Coolors](https://coolors.co/) - Gerador de paletas
- [Adobe Color](https://color.adobe.com/) - Ferramenta de cores
- [Color Hunt](https://colorhunt.co/) - Paletas prontas

### Google Fonts
- [Google Fonts](https://fonts.google.com/) - Biblioteca de fontes
- [Font Pair](https://fontpair.co/) - Combinações de fontes

### Ferramentas de Design
- [CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp) - Tutorial
- [CSS Units](https://www.w3schools.com/css/css_units.asp) - Unidades

---

*🎯 **Dica de Estudo**: Pratique muito com o Box Model - é fundamental para layouts profissionais!*

