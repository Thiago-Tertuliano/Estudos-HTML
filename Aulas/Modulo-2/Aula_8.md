# 🎨 Módulo 2 – Aula 8: Responsividade com Media Queries

## 🎯 Objetivos da Aula
- Compreender o conceito de responsividade
- Aprender a usar Media Queries
- Definir breakpoints adequados
- Criar layouts responsivos
- Testar sites em diferentes dispositivos

---

## 🧠 O que é Responsividade?

**Responsividade** é quando um site se adapta automaticamente ao tamanho da tela do usuário, mantendo a usabilidade e legibilidade em qualquer dispositivo.

### Por que Responsividade é Importante?

| Benefício | Descrição |
|-----------|-----------|
| **Experiência do usuário** | Site funciona bem em qualquer dispositivo |
| **SEO** | Google prioriza sites responsivos |
| **Acessibilidade** | Facilita uso por pessoas com necessidades especiais |
| **Manutenção** | Um código para todos os dispositivos |

### Dispositivos Comuns
- 📱 **Smartphones** (320px - 480px)
- 📱 **Tablets** (768px - 1024px)
- 💻 **Notebooks** (1024px - 1440px)
- 🖥️ **Desktops** (1440px+)

---

## 🔧 Media Queries: O Coração da Responsividade

### Sintaxe Básica
```css
@media (condição) {
  /* CSS aplicado quando a condição for verdadeira */
}
```

### Tipos de Media Queries

#### 1. Por Largura da Tela
```css
/* Telas menores que 600px */
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}

/* Telas maiores que 768px */
@media (min-width: 768px) {
  .container {
    max-width: 1200px;
  }
}

/* Telas entre 600px e 1024px */
@media (min-width: 600px) and (max-width: 1024px) {
  .sidebar {
    display: none;
  }
}
```

#### 2. Por Orientação
```css
/* Dispositivo em modo paisagem */
@media (orientation: landscape) {
  .header {
    height: 60px;
  }
}

/* Dispositivo em modo retrato */
@media (orientation: portrait) {
  .header {
    height: 80px;
  }
}
```

---

## 📐 Breakpoints Comuns

### Valores de Referência

| Dispositivo | Largura Máxima | Uso |
|-------------|----------------|-----|
| **Celulares pequenos** | 480px | `@media (max-width: 480px)` |
| **Celulares médios** | 600px | `@media (max-width: 600px)` |
| **Tablets** | 768px | `@media (max-width: 768px)` |
| **Notebooks** | 1024px | `@media (max-width: 1024px)` |
| **Telas grandes** | 1200px+ | `@media (min-width: 1200px)` |

### Abordagem Mobile-First
```css
/* Base para mobile (menor tela) */
.container {
  width: 100%;
  padding: 10px;
}

/* Tablet e acima */
@media (min-width: 768px) {
  .container {
    width: 90%;
    max-width: 800px;
    margin: 0 auto;
  }
}

/* Desktop e acima */
@media (min-width: 1024px) {
  .container {
    max-width: 1200px;
  }
}
```

---

## 🧪 Exemplo Prático Completo

### HTML
```html
<div class="banner">
  <h1>Bem-vindo ao meu site</h1>
  <p>Um site totalmente responsivo</p>
</div>

<div class="cards">
  <div class="card">Card 1</div>
  <div class="card">Card 2</div>
  <div class="card">Card 3</div>
</div>
```

### CSS Responsivo
```css
/* Estilos base (mobile-first) */
.banner {
  background-color: #0066cc;
  color: white;
  padding: 30px;
  text-align: center;
  font-size: 24px;
}

.cards {
  display: flex;
  flex-direction: column;
  gap: 20px;
  padding: 20px;
}

.card {
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 8px;
  text-align: center;
}

/* Tablet (768px e acima) */
@media (min-width: 768px) {
  .banner {
    padding: 40px;
    font-size: 32px;
  }
  
  .cards {
    flex-direction: row;
    justify-content: space-between;
  }
  
  .card {
    flex: 1;
    margin: 0 10px;
  }
}

/* Desktop (1024px e acima) */
@media (min-width: 1024px) {
  .banner {
    padding: 60px;
    font-size: 40px;
  }
  
  .cards {
    max-width: 1200px;
    margin: 0 auto;
  }
}
```

---

## ✅ Exercício Prático

### 📝 Tarefa
Torne sua página responsiva adicionando Media Queries ao seu `style.css`.

### 🎯 CSS Responsivo

```css
/* Estilos base (mobile-first) */
body {
  font-size: 16px;
  line-height: 1.5;
}

.container {
  width: 100%;
  padding: 15px;
}

.card {
  width: 100%;
  margin: 10px 0;
  padding: 15px;
}

.flex-container {
  flex-direction: column;
  gap: 15px;
}

.caixa {
  width: 100%;
  height: 80px;
}

/* Tablet (768px e acima) */
@media (min-width: 768px) {
  .container {
    max-width: 90%;
    margin: 0 auto;
  }
  
  .card {
    width: 45%;
    margin: 10px;
  }
  
  .flex-container {
    flex-direction: row;
    justify-content: space-around;
  }
  
  .caixa {
    width: 30%;
    height: 100px;
  }
}

/* Desktop (1024px e acima) */
@media (min-width: 1024px) {
  .container {
    max-width: 1200px;
  }
  
  .card {
    width: 30%;
  }
  
  .caixa {
    width: 25%;
  }
}

/* Telas muito pequenas (320px e abaixo) */
@media (max-width: 320px) {
  body {
    font-size: 14px;
  }
  
  .card {
    padding: 10px;
  }
  
  .caixa {
    height: 60px;
  }
}
```

### 💡 Dicas para o Exercício
- **Use mobile-first** como abordagem
- **Teste em diferentes tamanhos** de tela
- **Ajuste fontes** para cada breakpoint
- **Mantenha a usabilidade** em todos os dispositivos
- **Use o DevTools** para testar

---

## 🧪 Testes e Experimentos

### Teste 1: Diferentes Breakpoints
```css
/* Teste com breakpoints específicos */
@media (max-width: 480px) {
  /* Estilos para celulares pequenos */
}

@media (min-width: 481px) and (max-width: 768px) {
  /* Estilos para tablets */
}

@media (min-width: 769px) {
  /* Estilos para desktop */
}
```

### Teste 2: Orientação do Dispositivo
```css
/* Modo paisagem */
@media (orientation: landscape) {
  .header {
    height: 50px;
  }
}

/* Modo retrato */
@media (orientation: portrait) {
  .header {
    height: 80px;
  }
}
```

### Teste 3: Densidade de Pixels
```css
/* Dispositivos de alta resolução */
@media (-webkit-min-device-pixel-ratio: 2) {
  .icon {
    background-image: url('icon@2x.png');
  }
}
```

---

## 💡 Boas Práticas

### Unidades Responsivas
```css
/* ✅ Prefira unidades relativas */
.container {
  width: 90%;
  max-width: 1200px;
  font-size: 1rem;
  padding: 1em;
}

/* ❌ Evite unidades fixas */
.container {
  width: 800px;
  font-size: 16px;
  padding: 20px;
}
```

### Imagens Responsivas
```css
img {
  max-width: 100%;
  height: auto;
}

/* Imagens de fundo responsivas */
.banner {
  background-image: url('banner-mobile.jpg');
}

@media (min-width: 768px) {
  .banner {
    background-image: url('banner-desktop.jpg');
  }
}
```

### Flexbox Responsivo
```css
.container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.item {
  flex: 1 1 300px; /* Cresce, encolhe, base de 300px */
}
```

---

## 🔍 Como Testar Responsividade

### 1. DevTools do Navegador
- **F12** → Toggle device toolbar
- **Selecione dispositivos** específicos
- **Teste diferentes resoluções**

### 2. Ferramentas Online
- [Responsive Design Checker](https://responsivedesignchecker.com/)
- [Am I Responsive](https://ui.dev/amiresponsive)
- [Screenfly](https://bluetree.ai/screenfly/)

### 3. Dispositivos Reais
- **Smartphones** diferentes
- **Tablets** variados
- **Monitores** de diferentes tamanhos

---

## 🚀 Final do Módulo 2

### ✅ O que você aprendeu:
- **Estrutura páginas** com HTML semântico
- **Estiliza com CSS** básico e avançado
- **Usa Flexbox** para layouts modernos
- **Torna tudo responsivo** com Media Queries

### 🎯 Próximos Passos:
- 📚 **CSS Grid** para layouts complexos
- 🎨 **Animações e transições** CSS
- 🚀 **Frameworks** como Bootstrap
- 💻 **JavaScript** para interatividade

---

## 📚 Recursos Adicionais

### Documentação
- [MDN - Media Queries](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Media_Queries)
- [CSS-Tricks - Media Queries](https://css-tricks.com/logic-in-media-queries/)

### Ferramentas
- [Responsive Design Checker](https://responsivedesignchecker.com/)
- [Am I Responsive](https://ui.dev/amiresponsive)
- [BrowserStack](https://www.browserstack.com/) - Teste em dispositivos reais

### Guias
- [Responsive Web Design](https://www.w3schools.com/css/css_rwd_intro.asp)
- [Mobile-First Design](https://www.lukew.com/ff/entry.asp?933)

---

*🎯 **Dica de Estudo**: Sempre teste em dispositivos reais - o DevTools é útil, mas não substitui a experiência real!*