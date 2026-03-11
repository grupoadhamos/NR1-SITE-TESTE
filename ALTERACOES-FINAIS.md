# 🔧 **ALTERAÇÕES FINAIS - INSTRUÇÕES COMPLETAS**

## ✅ **O QUE SERÁ FEITO:**

1. ✅ Remover seção FAQ do site
2. ✅ Criar PDF com FAQ para estudo
3. ✅ Remover seção E-book (guardar para futuro)
4. ✅ Adicionar logo Adhamos em todo site
5. ✅ Remover linha azul do botão WhatsApp
6. ✅ Trocar "Diagnóstico" por "Consultoria"
7. ✅ Fazer contador de dias até 26/05/2025 funcionar

---

## 📝 **ALTERAÇÕES NO index.html:**

### **1. REMOVER SEÇÃO E-BOOK (Linhas 574-721)**

Deletar tudo desde:
```html
<!-- E-book Section -->
```

Até:
```html
</section>
```
(Antes do `<!-- FAQ Section -->`)

---

### **2. REMOVER SEÇÃO FAQ (Linhas 723-813)**

Deletar tudo desde:
```html
<!-- FAQ Section -->
```

Até:
```html
</section>
```
(Antes do `<!-- Final CTA Section -->`)

---

### **3. TROCAR "Diagnóstico" por "Consultoria"**

Usar buscar e substituir (Ctrl+H):

**Buscar:** `Diagnóstico`  
**Substituir:** `Consultoria`  
**Substituir todos**

**Buscar:** `diagnóstico`  
**Substituir:** `consultoria`  
**Substituir todos**

**Buscar:** `DIAGNÓSTICO`  
**Substituir:** `CONSULTORIA`  
**Substituir todos**

---

### **4. ADICIONAR LOGO ADHAMOS**

#### **No `<head>`, adicionar:**

Encontre a linha com:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
```

Logo APÓS, adicione:
```html
    
    <!-- Favicon -->
    <link rel="icon" type="image/png" href="https://www.genspark.ai/api/files/s/Vlo5ISsB">
```

#### **No HERO, após container:**

Encontre:
```html
<div class="container">
    <div class="hero-badge">
```

ANTES do `<div class="hero-badge">`, adicione:
```html
    <div class="logo-container">
        <img src="https://www.genspark.ai/api/files/s/Vlo5ISsB" alt="Adhamos" class="site-logo">
    </div>
    
```

#### **No FOOTER, antes do h3:**

Encontre:
```html
<div class="footer-brand">
    <h3>Adhamos</h3>
```

SUBSTITUA por:
```html
<div class="footer-brand">
    <img src="https://www.genspark.ai/api/files/s/Vlo5ISsB" alt="Adhamos" class="footer-logo">
    <h3>Adhamos</h3>
```

---

## 🎨 **ALTERAÇÕES NO css/style.css:**

### **1. REMOVER LINHA AZUL DO WHATSAPP**

Encontre:
```css
.whatsapp-float {
```

Dentro desse bloco, adicione:
```css
    text-decoration: none;
    border: none;
    outline: none;
```

Também adicione no hover:
```css
.whatsapp-float:hover {
    transform: scale(1.1);
    box-shadow: 0 6px 30px rgba(37, 211, 102, 0.6);
    text-decoration: none;
}
```

### **2. ADICIONAR ESTILOS DO LOGO**

No final da seção de estilos do header/hero, adicione:

```css
/* Logo Styles */
.logo-container {
    text-align: center;
    margin-bottom: 2rem;
}

.site-logo {
    width: 150px;
    height: auto;
    filter: drop-shadow(0 4px 10px rgba(0, 0, 0, 0.2));
}

.footer-logo {
    width: 80px;
    height: auto;
    margin-bottom: 1rem;
}

@media (max-width: 768px) {
    .site-logo {
        width: 100px;
    }
    
    .footer-logo {
        width: 60px;
    }
}
```

---

## ⏰ **ALTERAÇÕES NO js/main.js:**

### **Atualizar Contador de Dias Restantes**

Encontre a função `updateCountdown()` e SUBSTITUA por:

```javascript
// Contador regressivo
function updateCountdown() {
    const targetDate = new Date('2025-05-26T00:00:00').getTime();
    const now = new Date().getTime();
    const distance = targetDate - now;
    
    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    
    // Atualiza contador no sticky banner
    const stickyCountdown = document.getElementById('stickyCountdown');
    if (stickyCountdown) {
        stickyCountdown.textContent = `⏰ ${days} dias restantes`;
    }
    
    // Atualiza o número "365 dias para adequar" com dias reais restantes
    const statNumbers = document.querySelectorAll('.stat-number');
    statNumbers.forEach(stat => {
        if (stat.textContent === '365') {
            stat.textContent = days;
        }
    });
    
    console.log(`Faltam ${days} dias, ${hours} horas e ${minutes} minutos para 26/05/2025`);
}

// Atualiza contador imediatamente e a cada minuto
updateCountdown();
setInterval(updateCountdown, 60000);
```

---

## 📄 **PDF DO FAQ - CONTEÚDO**

Vou criar um arquivo separado com todo o conteúdo do FAQ para você transformar em PDF de estudo.

Arquivo: `FAQ-ESTUDO-NR1.md`

---

## 🗂️ **ARQUIVOS DO E-BOOK (GUARDADO)**

Vou criar um arquivo separado com toda a seção do e-book para uso futuro.

Arquivo: `EBOOK-SECTION-GUARDADO.html`

---

## ✅ **PASSO A PASSO PARA APLICAR:**

### **OPÇÃO A: Editar no Servidor (Recomendado)**

1. **Acessar Gerenciador de Arquivos**
2. **Abrir `index.html` para editar**
3. **Aplicar mudanças conforme acima:**
   - Deletar seção e-book
   - Deletar seção FAQ
   - Buscar e substituir "Diagnóstico" por "Consultoria"
   - Adicionar logos
4. **Salvar**
5. **Abrir `css/style.css`**
6. **Aplicar mudanças de CSS**
7. **Salvar**
8. **Abrir `js/main.js`**
9. **Atualizar função do contador**
10. **Salvar**
11. **Testar site**

### **OPÇÃO B: Baixar, Editar, Upload**

1. **Baixar arquivos:**
   - `index.html`
   - `css/style.css`
   - `js/main.js`

2. **Editar localmente** (use Notepad++ ou VS Code)

3. **Aplicar todas as mudanças**

4. **Fazer upload** de volta (substituir arquivos)

---

## 🧪 **TESTES APÓS APLICAR:**

- [ ] Logo aparece no topo
- [ ] Logo aparece no footer
- [ ] Favicon aparece na aba do navegador
- [ ] Seção E-book não aparece mais
- [ ] Seção FAQ não aparece mais
- [ ] Todas as menções são "Consultoria" (não Diagnóstico)
- [ ] Botão WhatsApp sem linha azul
- [ ] Contador mostra dias corretos até 26/05/2025
- [ ] Número no hero também atualiza (não é mais fixo 365)

---

## 📞 **PRECISA DE AJUDA?**

Se tiver dúvida em qualquer etapa, me avise! 😊

---

Vou agora criar os arquivos complementares...