# 🎨 Módulo 2 – Aula 7: Layout com Flexbox

## 🎯 Objetivos da Aula
- Compreender o conceito de Flexbox
- Aprender propriedades do container flex
- Dominar propriedades dos itens flex
- Criar layouts responsivos com Flexbox
- Centralizar elementos de forma eficiente

---

## 🧠 O que é Flexbox?

**Flexbox** (Flexible Box Layout) é um modo de layout em CSS que facilita o posicionamento e o dimensionamento de itens dentro de um container flexível.

### Vantagens do Flexbox
- 🎯 **Centralização fácil** de elementos
- 📐 **Layouts responsivos** automáticos
- 🔄 **Reordenação** de elementos
- ⚖️ **Distribuição** automática de espaço
- 📱 **Adaptação** a diferentes telas

### Ativação do Flexbox
```css
.container {
  display: flex;
}
```

---

## 📦 Termos-Chave do Flexbox

### Estrutura Básica
```
┌─────────────────────────────────┐
│        CONTAINER FLEX           │
│  ┌─────┐  ┌─────┐  ┌─────┐      │
│  │ITEM1│  │ITEM2│  │ITEM3│      │
│  └─────┘  └─────┘  └─────┘      │
└─────────────────────────────────┘
```

### Definições
- **Container**: Elemento com `display: flex`
- **Itens**: Filhos diretos do container
- **Eixo Principal**: Direção definida por `flex-direction`
- **Eixo Transversal**: Perpendicular ao eixo principal

---

## 🔧 Propriedades do Container Flex

### Propriedades Principais

| Propriedade | Função | Valores |
|-------------|--------|---------|
| `display` | Ativa o flexbox | `flex`, `inline-flex` |
| `flex-direction` | Direção dos itens | `row`, `column`, `row-reverse`, `column-reverse` |
| `justify-content` | Alinhamento no eixo principal | `flex-start`, `center`, `flex-end`, `space-between`, `space-around`, `space-evenly` |
| `align-items` | Alinhamento no eixo transversal | `stretch`, `flex-start`, `center`, `flex-end`, `baseline` |
| `gap` | Espaçamento entre itens | `10px`, `1rem`, etc. |

### Exemplos Práticos

#### 1. Layout Horizontal
```css
.container {
  display: flex;
  flex-direction: row;           /* Padrão */
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}
```

#### 2. Layout Vertical
```css
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 15px;
}
```

#### 3. Centralização Perfeita
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
```

---

## 📋 Propriedades dos Itens Flex

### Propriedades Principais

| Propriedade | Função | Valores |
|-------------|--------|---------|
| `flex-grow` | Permite crescer | `0`, `1`, `2`, etc. |
| `flex-shrink` | Permite encolher | `0`, `1`, `2`, etc. |
| `flex-basis` | Tamanho inicial | `auto`, `0`, `200px`, etc. |
| `flex` | Atalho para as 3 acima | `1`, `0 1 auto`, etc. |
| `align-self` | Alinhamento individual | `auto`, `flex-start`, `center`, `flex-end` |

### Exemplos Práticos

#### 1. Item que cresce
```css
.item {
  flex: 1;  /* Equivale a flex-grow: 1, flex-shrink: 1, flex-basis: 0% */
}
```

#### 2. Item com tamanho fixo
```css
.item {
  flex: 0 0 200px;  /* Não cresce, não encolhe, 200px de base */
}
```

#### 3. Item que ocupa espaço disponível
```css
.item {
  flex-grow: 1;
  flex-shrink: 1;
  flex-basis: auto;
}
```

---

## ✏️ Exemplo Prático Completo

### HTML
```html
<div class="container">
  <div class="box">1</div>
  <div class="box">2</div>
  <div class="box">3</div>
</div>
```

### CSS
```css
.container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 200px;
  background-color: #eee;
  padding: 20px;
  gap: 15px;
}

.box {
  background-color: #0066cc;
  color: white;
  padding: 20px;
  font-size: 20px;
  border-radius: 8px;
  min-width: 80px;
  text-align: center;
}
```

---

## 🎨 Direções do Flexbox

### flex-direction: row (padrão)
```
┌─────────────────────────────────┐
│  [1]  [2]  [3]                  │
└─────────────────────────────────┘
```

### flex-direction: column
```
┌─────────┐
│   [1]   │
│   [2]   │
│   [3]   │
└─────────┘
```

### flex-direction: row-reverse
```
┌─────────────────────────────────┐
│                [3]  [2]  [1]    │
└─────────────────────────────────┘
```

### flex-direction: column-reverse
```
┌─────────┐
│   [3]   │
│   [2]   │
│   [1]   │
└─────────┘
```

---

## ✅ Exercício Prático

### 📝 Tarefa
Crie uma section com 3 caixas (divs com a classe `caixa`) envolvidas por um container com a classe `flex-container`.

### 🎯 Estrutura HTML

```html
<section class="flex-container">
  <div class="caixa">1</div>
  <div class="caixa">2</div>
  <div class="caixa">3</div>
</section>
```

### 🎨 Estilos CSS

```css
.flex-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #ddd;
  min-height: 200px;
  gap: 20px;
}

.caixa {
  width: 100px;
  height: 100px;
  background-color: #0066cc;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: bold;
  font-size: 24px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.caixa:hover {
  background-color: #0052a3;
  transform: scale(1.05);
  transition: all 0.3s ease;
}
```

### 💡 Dicas para o Exercício
- **Teste diferentes valores** de `justify-content`
- **Experimente `flex-direction: column`**
- **Teste `align-items`** com diferentes valores
- **Adicione `gap`** para espaçamento
- **Use `flex-wrap`** para quebra de linha

---

## 🧪 Testes e Experimentos

### Teste 1: Diferentes Alinhamentos
```css
/* Centralizar */
.flex-container {
  justify-content: center;
}

/* Distribuir igualmente */
.flex-container {
  justify-content: space-evenly;
}

/* Espaçamento nas extremidades */
.flex-container {
  justify-content: space-between;
}
```

### Teste 2: Direções Diferentes
```css
/* Layout vertical */
.flex-container {
  flex-direction: column;
  justify-content: center;
}

/* Inverter ordem horizontal */
.flex-container {
  flex-direction: row-reverse;
}
```

### Teste 3: Itens Flexíveis
```css
/* Itens que crescem igualmente */
.caixa {
  flex: 1;
  margin: 0 10px;
}

/* Item central maior */
.caixa:nth-child(2) {
  flex: 2;
}
```

---

## 💡 Centralização Perfeita

### Centralizar na Tela
```css
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
```

### Centralizar em Container
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 300px;
}
```

---

## 🔍 Próximos Passos
- ✅ Dominar Flexbox básico
- 📚 Aprender sobre CSS Grid
- 🎨 Explorar layouts responsivos
- 🚀 Criar layouts complexos

---

## 📚 Recursos Adicionais

### Documentação
- [MDN - Flexbox](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [CSS-Tricks - Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

### Ferramentas
- [Flexbox Froggy](https://flexboxfroggy.com/) - Jogo para aprender Flexbox
- [Flexbox Playground](https://codepen.io/enxaneta/full/adLPwv/) - Sandbox interativo

### Guias Visuais
- [Flexbox Cheat Sheet](https://yoksel.github.io/flex-cheatsheet/)
- [Flexbox Visual Guide](https://www.flexbox.help/)

---

*🎯 **Dica de Estudo**: Pratique muito com Flexbox - é essencial para layouts modernos!*
