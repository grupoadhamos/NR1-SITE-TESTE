# 📄 COMO GERAR O PDF DAS FAQs NR-1

## 🎯 OBJETIVO
Transformar o arquivo `FAQ-NR1-ADHAMOS.md` em um PDF profissional para enviar aos clientes.

---

## 🚀 MÉTODO 1: ONLINE (MAIS RÁPIDO)

### Opção A: Markdown to PDF (Recomendado)
1. Acesse: **https://www.markdowntopdf.com/**
2. Clique em "Choose File" ou arraste `FAQ-NR1-ADHAMOS.md`
3. Aguarde conversão (2-3 segundos)
4. Clique em "Download PDF"
5. Pronto! ✅

**Vantagens:**
- ✅ Rápido (menos de 30 segundos)
- ✅ Não precisa instalar nada
- ✅ Gratuito
- ✅ Formatação automática

---

### Opção B: Pandoc Online
1. Acesse: **https://pandoc.org/try/**
2. Cole o conteúdo do arquivo `FAQ-NR1-ADHAMOS.md`
3. Selecione "Output format: PDF"
4. Clique em "Convert"
5. Download automático

---

### Opção C: Dillinger (Editor Online)
1. Acesse: **https://dillinger.io/**
2. Clique em "Import from" → "Choose File"
3. Selecione `FAQ-NR1-ADHAMOS.md`
4. Clique em "Export as" → "PDF"
5. Salve o arquivo

**Vantagem extra:**
- ✅ Pré-visualização em tempo real
- ✅ Editor online profissional

---

## 💻 MÉTODO 2: VSCode (PROFISSIONAL)

### Passo 1: Instalar Extensão
1. Abra VSCode
2. Vá em Extensions (Ctrl+Shift+X)
3. Busque: **"Markdown PDF"**
4. Instale a extensão de **yzane**
5. Aguarde instalação

### Passo 2: Converter
1. Abra o arquivo `FAQ-NR1-ADHAMOS.md` no VSCode
2. Pressione **Ctrl+Shift+P** (ou Cmd+Shift+P no Mac)
3. Digite: **"Markdown PDF: Export (pdf)"**
4. Enter
5. PDF será salvo na mesma pasta

**Tempo total:** ~1 minuto

---

## 🖥️ MÉTODO 3: LINHA DE COMANDO (AVANÇADO)

### Usando Pandoc (Instalar primeiro)

**Windows:**
```bash
# Baixe em: https://pandoc.org/installing.html
# Depois execute:
pandoc FAQ-NR1-ADHAMOS.md -o FAQ-NR1-ADHAMOS.pdf
```

**Mac (com Homebrew):**
```bash
brew install pandoc
pandoc FAQ-NR1-ADHAMOS.md -o FAQ-NR1-ADHAMOS.pdf
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt-get install pandoc
pandoc FAQ-NR1-ADHAMOS.md -o FAQ-NR1-ADHAMOS.pdf
```

---

## 🎨 PERSONALIZAR O PDF (OPCIONAL)

### Adicionar Cabeçalho e Rodapé (Pandoc):
```bash
pandoc FAQ-NR1-ADHAMOS.md -o FAQ-NR1-ADHAMOS.pdf \
  --pdf-engine=xelatex \
  --variable mainfont="Arial" \
  --variable fontsize=12pt \
  --variable geometry:margin=2cm \
  --toc \
  --toc-depth=2
```

### Usando CSS Customizado (VSCode):
1. Crie arquivo `pdf-style.css`:
```css
body {
    font-family: Arial, sans-serif;
    font-size: 12pt;
    line-height: 1.6;
}

h1 {
    color: #006465;
    font-size: 24pt;
    border-bottom: 3px solid #beee3b;
    padding-bottom: 10px;
}

h2 {
    color: #0f928c;
    font-size: 18pt;
    margin-top: 20px;
}

table {
    border-collapse: collapse;
    width: 100%;
}

th, td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: left;
}
```

2. Configure VSCode `settings.json`:
```json
"markdown-pdf.styles": ["pdf-style.css"]
```

---

## 📋 CHECKLIST PÓS-CONVERSÃO

Após gerar o PDF, verifique:

- [ ] Todas as 8 perguntas estão visíveis
- [ ] Formatação dos títulos está correta
- [ ] Tabelas estão legíveis
- [ ] Listas numeradas/marcadores funcionam
- [ ] Não há quebras estranhas de página
- [ ] Logo Adhamos aparece (se adicionou)
- [ ] Informações de contato estão corretas
- [ ] Tamanho do arquivo é razoável (< 2 MB)

---

## 🔧 PROBLEMAS COMUNS

### PDF com formatação quebrada:
**Solução:** Use método online (Markdown to PDF) que cuida da formatação automaticamente

### Tabelas cortadas:
**Solução:** Reduza largura das colunas ou converta tabela em lista

### Caracteres especiais (acentos):
**Solução:** Salve o .md com encoding UTF-8

### PDF muito grande:
**Solução:** Comprima em https://www.ilovepdf.com/compress_pdf

---

## 🎯 RECOMENDAÇÃO FINAL

**Para resultados rápidos e profissionais:**

👉 Use **https://www.markdowntopdf.com/**

**Passos:**
1. Acesse o site
2. Upload do arquivo `.md`
3. Download do PDF
4. **Pronto em menos de 1 minuto!**

---

## 📤 COMO ENVIAR PARA CLIENTES

### Opção 1: E-mail Direto
```
Assunto: FAQ - Riscos Psicossociais NR-1 | Adhamos

Olá [Nome do Cliente],

Segue em anexo nosso Guia Completo de Perguntas Frequentes 
sobre a NR-1 e Riscos Psicossociais.

Neste material você encontrará:
✅ 8 perguntas essenciais respondidas
✅ Cronogramas e prazos
✅ Custos da não conformidade
✅ Como funciona nossa consultoria

Qualquer dúvida, estou à disposição!

Atenciosamente,
Andrey Henrique
Adhamos - Especialistas em Riscos Psicossociais
WhatsApp: (11) 96394-3271
```

### Opção 2: Link no WhatsApp
1. Suba PDF no Google Drive
2. Configure para "Qualquer pessoa com o link pode ver"
3. Copie link
4. Envie no WhatsApp:
```
Olá! 👋

Preparei um material completo sobre a NR-1 para você:

📄 FAQ - Riscos Psicossociais NR-1
[LINK DO GOOGLE DRIVE]

São 8 perguntas essenciais que todo gestor 
precisa saber sobre adequação à nova norma.

Vale a pena dar uma olhada! 😊
```

### Opção 3: Download no Site
1. Suba PDF na pasta `downloads/` do site
2. Crie botão de download no `index.html`:
```html
<a href="downloads/FAQ-NR1-ADHAMOS.pdf" download class="btn btn-secondary">
    <i class="fas fa-download"></i>
    BAIXAR FAQ EM PDF
</a>
```

---

## ✅ PRONTO!

Agora você sabe **3 métodos diferentes** para gerar o PDF das FAQs. 

**Recomendação:** Comece com o método online para testar, depois use VSCode se precisar fazer ajustes frequentes.

---

**Precisa de ajuda?** Me avise se tiver problemas na conversão! 🚀
