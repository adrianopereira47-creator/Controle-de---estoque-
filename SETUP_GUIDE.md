# 📱 Guia de Configuração - App Controle de Estoque

## ✅ O que foi criado

Seus arquivos PWA (Progressive Web App) já estão prontos para funcionarem!

### Arquivos criados:
1. **manifest.json** - Configurações do app (nome, ícone, tema)
2. **index.html** - Página inicial com interface moderna
3. **sw.js** - Service Worker para funcionar offline
4. **SETUP_GUIDE.md** - Este arquivo

## 🎨 Próximos passos: Criar os Ícones

### Opção 1: Gerar automaticamente (RECOMENDADO)
Use o **PWA Asset Generator**:
1. Vá para: https://www.pwabuilder.com/
2. Clique em "Generate" e faça upload de uma imagem PNG (mínimo 512x512px)
3. Ele gera todos os ícones automaticamente
4. Baixe os ícones e coloque na pasta `/images/`

### Opção 2: Criar manualmente
Você precisa de 4 arquivos de imagem PNG na pasta `/images/`:
- `icon-192x192.png` (192x192 pixels)
- `icon-512x512.png` (512x512 pixels)
- `icon-maskable-192x192.png` (192x192 pixels)
- `icon-maskable-512x512.png` (512x512 pixels)

**Requisitos:**
- Formato: PNG com fundo transparente
- Tamanho: conforme especificado
- Sem bordas arredondadas (o sistema adiciona automaticamente)

### Opção 3: Usar ferramentas online gratuitas
- **Favicon Generator**: https://www.favicon-generator.org/
- **Real Favicon Generator**: https://realfavicongenerator.net/
- **Image Resizer**: https://www.birme.net/

## 📂 Estrutura de pastas esperada

```
seu-projeto/
├── index.html
├── manifest.json
├── sw.js
├── SETUP_GUIDE.md
├── images/
│   ├── icon-192x192.png
│   ├── icon-512x512.png
│   ├── icon-maskable-192x192.png
│   └── icon-maskable-512x512.png
└── README.md
```

## 🚀 Como testar

### No navegador:
1. Abra `index.html` no seu navegador
2. Se vier um botão "Instalar na Tela Inicial" → clique nele
3. Se não aparecer → use o menu do navegador

### No Android:
1. Abra no Chrome/Firefox
2. Clique no menu (⋮) 
3. Selecione "Instalar aplicativo" ou "Adicionar à tela inicial"

### No iOS:
1. Abra no Safari
2. Clique em Compartilhar (↑)
3. Selecione "Adicionar à Tela Inicial"

## 🎯 Configurações personalizáveis

### Mudar cores do app (em `manifest.json`):
```json
"theme_color": "#007bff",      // Cor da barra superior
"background_color": "#ffffff"   // Cor de fundo ao abrir
```

### Mudar nome do app:
```json
"name": "Seu Nome Aqui",           // Nome completo
"short_name": "Nome Curto"         // Nome exibido no ícone
```

### Mudar página inicial:
```json
"start_url": "/"  // Mude para o caminho desejado
```

## ⚙️ Service Worker (Funcionalidade Offline)

O `sw.js` permite que o app funcione offline:
- ✅ Cacheia automaticamente páginas visitadas
- ✅ Funciona sem internet depois da primeira visita
- ✅ Atualiza o cache quando há conexão

Para desabilitar: remova a referência em `index.html`:
```html
<!-- Remova esta linha para desabilitar offline -->
<script>
  navigator.serviceWorker.register('/sw.js');
</script>
```

## 🔐 Deploy e hosting

### Requisito importante:
**O app DEVE ser servido via HTTPS** para funcionar corretamente (exceto localhost).

### Opções de hosting gratuito:
- **GitHub Pages**: https://pages.github.com/
- **Vercel**: https://vercel.com/
- **Netlify**: https://www.netlify.com/
- **Firebase Hosting**: https://firebase.google.com/products/hosting

## 📱 Compartilhar com usuários

Após fazer upload para um servidor:

**Android:**
1. Envie o link da página
2. Usuário abre no Chrome → Menu → Instalar

**iOS:**
1. Envie o link no Safari
2. Usuário abre → Compartilhar → Adicionar à Tela Inicial

## ❓ Dúvidas comuns

**P: Por que não aparece o botão "Instalar"?**
A: Alguns navegadores antigos não suportam PWA. Use versões recentes.

**P: Posso mudar o ícone depois?**
A: Sim, atualize os arquivos em `/images/` e limpe o cache do navegador.

**P: Funciona completamente offline?**
A: Sim, após a primeira visita. A funcionalidade é limitada ao que foi cacheado.

**P: Como remover o app instalado?**
A: Android: Segure o ícone → Desinstalar. iOS: Segure → Remover app.

---

## 🎉 Tudo pronto!

Você tem um Progressive Web App funcional! Agora é só adicionar os ícones e fazer o deploy. 🚀
