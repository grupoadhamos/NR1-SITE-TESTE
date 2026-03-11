# 🎨 COMO ADICIONAR O LOGO ADHAMOS NO SITE

## ✅ O QUE JÁ FOI FEITO

Todos os códigos necessários para exibir o logo foram implementados. O site está **pronto** para receber a imagem do logo.

---

## 📂 ONDE COLOCAR O ARQUIVO DO LOGO

1. **Crie a pasta `images`** na raiz do projeto (se ainda não existir)
2. **Salve o arquivo do logo** com o nome: `logo-adhamos.png`
3. **Caminho final:** `images/logo-adhamos.png`

---

## 🖼️ ESPECIFICAÇÕES RECOMENDADAS

### Formato do Arquivo:
- **Formato:** PNG (com fundo transparente)
- **Alternativa:** SVG (vetorial - melhor qualidade)
- **Evitar:** JPG (não tem transparência)

### Dimensões Recomendadas:
- **Largura:** 600px a 1200px
- **Altura:** Proporcional ao logo
- **Resolução:** 72 dpi (web) ou 144 dpi (retina)

### Tamanho do Arquivo:
- **Ideal:** Até 100 KB
- **Máximo:** 500 KB
- Use compressão PNG (TinyPNG.com)

---

## 📍 ONDE O LOGO APARECERÁ

### 1️⃣ Hero Section (Topo da Página)
- **Tamanho na tela:** 280px de largura
- **Posição:** Centro, logo acima do badge de urgência
- **Efeito:** Hover com zoom suave e sombra

### 2️⃣ Footer (Rodapé)
- **Tamanho na tela:** 180px de largura  
- **Posição:** Acima do texto "Adhamos"
- **Efeito:** Hover com aumento de opacidade

### 3️⃣ Marca d'Água (Background)
- **Tamanho na tela:** 500px
- **Posição:** Centro da página, fixo
- **Opacidade:** 3% (bem sutil, não atrapalha leitura)
- **Efeito:** Fica atrás de todo o conteúdo

---

## 🔧 COMO TESTAR

### Opção 1: Upload Manual (Recomendado)
1. Acesse seu servidor/hospedagem
2. Navegue até a pasta do projeto
3. Crie a pasta `images` (se não existir)
4. Faça upload do arquivo `logo-adhamos.png`
5. Atualize a página e veja o logo aparecer

### Opção 2: Testar Localmente
1. Abra o projeto no VSCode
2. Crie a pasta `images` na raiz
3. Coloque o arquivo `logo-adhamos.png`
4. Use Live Server para visualizar

---

## ❌ SE O LOGO NÃO APARECER

### Verifique:
1. ✅ O arquivo está em `images/logo-adhamos.png`?
2. ✅ O nome está EXATAMENTE `logo-adhamos.png` (minúsculas)?
3. ✅ A pasta `images` está na raiz do projeto?
4. ✅ O arquivo não está corrompido?
5. ✅ O cache do navegador foi limpo? (Ctrl+F5)

### Estrutura de Pastas Esperada:
```
projeto/
│
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
├── images/
│   └── logo-adhamos.png  ← AQUI!
└── FAQ-NR1-ADHAMOS.md
```

---

## 🎨 PERSONALIZAÇÕES DISPONÍVEIS

### Mudar Tamanho do Logo no Hero:
Edite em `css/style.css`:
```css
.main-logo {
    max-width: 280px;  /* Aumente ou diminua */
}
```

### Mudar Tamanho do Logo no Footer:
```css
.footer-logo {
    max-width: 180px;  /* Aumente ou diminua */
}
```

### Desativar Marca d'Água:
Comente ou delete este trecho em `css/style.css`:
```css
body::before {
    /* ... toda a regra */
}
```

### Mudar Opacidade da Marca d'Água:
```css
body::before {
    opacity: 0.03;  /* Valores: 0 (invisível) a 1 (opaco) */
}
```

---

## 📱 RESPONSIVIDADE

O logo **já está responsivo**:

### Desktop (> 768px):
- Hero: 280px de largura
- Footer: 180px de largura

### Mobile (≤ 768px):
- Hero: Reduz automaticamente para 200px
- Footer: Reduz automaticamente para 150px

---

## 🚀 DEPOIS DE ADICIONAR O LOGO

### Checklist Final:
- [ ] Logo aparece no topo da página (Hero)
- [ ] Logo aparece no rodapé (Footer)
- [ ] Marca d'água sutil no fundo (opcional)
- [ ] Hover funciona no logo do Hero (zoom)
- [ ] Hover funciona no logo do Footer (opacidade)
- [ ] Logo está nítido em todas as resoluções
- [ ] Tamanho do arquivo é menor que 500 KB

---

## 💡 DICAS PRO

### 1. Otimize o Logo:
- Use **TinyPNG.com** para reduzir tamanho sem perder qualidade
- Converta para **WebP** para carregar 30% mais rápido

### 2. Fallback SVG:
Se tiver versão SVG do logo:
```html
<img src="images/logo-adhamos.svg" alt="Adhamos">
```

### 3. Logo Diferente para Mobile:
Crie versão horizontal e vertical:
- `logo-adhamos-horizontal.png` (para desktop)
- `logo-adhamos-vertical.png` (para mobile)

---

## 📞 PRECISA DE AJUDA?

Se o logo não aparecer ou tiver problemas:
1. Verifique o console do navegador (F12)
2. Confirme o caminho do arquivo
3. Teste com outro nome de arquivo
4. Me envie print do erro para ajudar

---

**Última atualização:** 2025-02-20  
**Status:** ✅ Código implementado, aguardando arquivo do logo
