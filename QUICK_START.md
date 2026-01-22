# 🚀 Guia de Início Rápido

## ⚡ 3 Passos para Começar

### 1️⃣ Personalize Seu Perfil

Abra `index.html` e edite:

**Seu Nome:**
```html
Linha 65: <span class="gradient-text typing-text">Seu Nome</span>
```

**Sua Descrição:**
```html
Linhas 69-75: Edite as palavras da descrição
```

**Suas Estatísticas:**
```html
Linhas 79-92: Atualize números de seguidores, views, etc.
```

### 2️⃣ Configure Seus Links

Encontre cada link social e atualize o `href`:

```html
<!-- Instagram - Linha ~110 -->
<a href="https://instagram.com/SEUUSUARIO"

<!-- YouTube - Linha ~129 -->
<a href="https://youtube.com/@SEUCANAL"

<!-- TikTok - Linha ~148 -->
<a href="https://tiktok.com/@SEUUSUARIO"

<!-- Twitter - Linha ~167 -->
<a href="https://twitter.com/SEUUSUARIO"

<!-- LinkedIn - Linha ~186 -->
<a href="https://linkedin.com/in/SEUUSUARIO"

<!-- GitHub - Linha ~205 -->
<a href="https://github.com/SEUUSUARIO"

<!-- Email - Linha ~224 -->
<a href="mailto:SEU@EMAIL.COM"

<!-- WhatsApp - Linha ~243 -->
<a href="https://wa.me/5511999999999"
```

### 3️⃣ Ative o Analytics (Opcional)

**Google Analytics 4:**
```html
Linha 29: Substitua 'G-XXXXXXXXXX' pelo seu ID
Linha 35: Substitua 'G-XXXXXXXXXX' pelo seu ID
```

**Facebook Pixel:**
```html
Linha 41: Substitua 'YOUR_PIXEL_ID' pelo seu Pixel ID
Linha 51: Substitua 'YOUR_PIXEL_ID' pelo seu Pixel ID
```

## 🎨 Customização Rápida de Cores

Edite `css/style.css` (linhas 13-17):

```css
--color-yellow: #FFD700;        /* Sua cor principal */
--color-yellow-light: #FFE55C;  /* Versão clara */
--color-yellow-dark: #E6C200;   /* Versão escura */
```

## 📤 Publicar o Site

### GitHub Pages (Grátis)
1. Crie repositório no GitHub
2. Faça upload de todos os arquivos
3. Settings → Pages → Source: main branch
4. Acesse: `usuario.github.io/nome-do-repo`

### Netlify (Grátis)
1. Arraste a pasta para netlify.com/drop
2. Site publicado instantaneamente!

### Hospedagem Própria
1. Faça upload via FTP
2. Coloque todos os arquivos na pasta raiz
3. Acesse seu domínio

## ✅ Checklist Antes de Publicar

- [ ] Atualizei meu nome
- [ ] Configurei minha descrição
- [ ] Atualizei as estatísticas
- [ ] Todos os links sociais estão corretos
- [ ] Email e WhatsApp configurados
- [ ] Testei o site localmente
- [ ] (Opcional) Analytics configurados
- [ ] Ícones carregando corretamente

## 🔍 Testar Localmente

1. Abra `index.html` em um navegador
2. Teste todos os links
3. Verifique responsividade (F12 → Device Toolbar)
4. Teste animações ao rolar a página

## 🆘 Problemas Comuns

**Partículas não aparecem?**
- Verifique se o arquivo `js/particles.js` está carregando
- Abra o console (F12) e veja se há erros

**Animações não funcionam?**
- Certifique-se que todos os arquivos JS estão carregando
- Verifique console para erros

**Links não funcionam?**
- Verifique se os URLs estão corretos
- Teste em modo de navegação anônima

**Ícones não aparecem?**
- Verifique conexão com internet (Font Awesome é CDN)
- Teste em outro navegador

## 📱 Redes Sociais Suportadas

✅ Instagram
✅ YouTube  
✅ TikTok
✅ Twitter/X
✅ LinkedIn
✅ GitHub
✅ Email
✅ WhatsApp

**Quer adicionar mais?** Veja seção "Adicionar Nova Rede Social" no README.md principal!

## 💡 Dicas Pro

1. **SEO**: Atualize meta tags no `<head>` do index.html
2. **Favicon**: Adicione seu próprio favicon (linha 20)
3. **Open Graph**: Customize imagens de compartilhamento (linha 24-26)
4. **Cores da Marca**: Use suas cores oficiais nas variáveis CSS
5. **Analytics**: Configure eventos personalizados em `js/tracking.js`

## 🎯 Próximos Passos

Depois de publicar:
1. Compartilhe o link em suas redes sociais
2. Adicione o link na bio do Instagram
3. Use em assinaturas de email
4. Monitore analytics para ver quais links são mais clicados

## 📚 Documentação Completa

Para informações detalhadas, consulte `README.md`

---

**Pronto para publicar? Vá para a aba Publish! 🚀**
