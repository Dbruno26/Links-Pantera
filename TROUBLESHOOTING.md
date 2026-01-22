# 🔧 Guia de Troubleshooting

## 🐛 Problemas Comuns e Soluções

### Problema: Site não carrega corretamente

**Sintomas:**
- Tela branca
- Nenhum conteúdo aparece
- Erros no console

**Soluções:**
```
1. Verifique se todos os arquivos estão na estrutura correta:
   - index.html (raiz)
   - css/style.css
   - js/particles.js
   - js/animations.js
   - js/cursor.js
   - js/tracking.js

2. Abra o Console do navegador (F12 → Console)
3. Procure por erros em vermelho
4. Verifique se os caminhos dos arquivos estão corretos
```

---

### Problema: Partículas não aparecem

**Sintomas:**
- Background está escuro/preto mas sem partículas animadas
- Canvas vazio

**Soluções:**
```
1. Verifique o Console (F12):
   - Procure por erros relacionados a particles.js

2. Certifique-se que o canvas existe:
   - Inspecione elemento (F12 → Elements)
   - Procure por <canvas id="particles-canvas">

3. Teste em outro navegador:
   - Pode ser problema de compatibilidade

4. Verifique JavaScript habilitado:
   - Configurações do navegador → JavaScript deve estar ON
```

---

### Problema: Animações não funcionam

**Sintomas:**
- Elementos aparecem de uma vez (sem fade in)
- Não há efeito ao rolar a página
- Texto não tem efeito de digitação

**Soluções:**
```
1. Verifique se animations.js está carregando:
   - Console (F12) → Network → Procure por animations.js
   - Deve aparecer status 200

2. Limpe o cache do navegador:
   - Ctrl+Shift+Delete (Windows/Linux)
   - Cmd+Shift+Delete (Mac)
   - Selecione "Cache" e limpe

3. Teste em modo anônimo:
   - Ctrl+Shift+N (Chrome)
   - Ctrl+Shift+P (Firefox)

4. Verifique "prefers-reduced-motion":
   - Sistema pode ter animações desabilitadas
   - Windows: Settings → Ease of Access → Display
   - Mac: System Preferences → Accessibility → Display
```

---

### Problema: Cursor customizado não aparece

**Sintomas:**
- Cursor padrão do sistema aparece
- Elementos .cursor e .cursor-follower não visíveis

**Soluções:**
```
1. Verifique se está em Desktop:
   - Cursor customizado só funciona em telas > 768px
   - Em mobile/tablet, cursor padrão é usado

2. Teste movimento do mouse:
   - Mova o mouse pela tela
   - Cursor deve aparecer após movimento

3. Verifique CSS:
   - Inspecione elementos .cursor e .cursor-follower
   - Devem ter opacity: 1 após movimento

4. Console log:
   - Procure por erros em cursor.js
```

---

### Problema: Links não funcionam

**Sintomas:**
- Click não redireciona
- Link não abre em nova aba

**Soluções:**
```
1. Verifique URL:
   - Deve começar com https://
   - Formato correto: https://instagram.com/usuario

2. Teste link direto:
   - Copie o href e cole no navegador
   - Se não funcionar, URL está incorreta

3. Verifique target="_blank":
   - Deve estar presente para abrir em nova aba

4. Teste sem tracking:
   - Desabilite temporariamente tracking.js
   - Se funcionar, problema está no tracking
```

---

### Problema: Ícones não aparecem (Font Awesome)

**Sintomas:**
- Quadrados vazios no lugar dos ícones
- Ícones com "?"

**Soluções:**
```
1. Verifique conexão de internet:
   - Font Awesome é carregado via CDN
   - Sem internet = sem ícones

2. Verifique CDN:
   - Console → Network → Procure por fontawesome
   - Status deve ser 200

3. Teste CDN alternativo:
   - Substitua link do Font Awesome no <head>
   - Use: https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css

4. Classes corretas:
   - Deve ser: <i class="fab fa-instagram"></i>
   - fab = brands, fas = solid, far = regular
```

---

### Problema: Google Analytics não rastreia

**Sintomas:**
- Nenhum dado no Google Analytics
- Console não mostra eventos

**Soluções:**
```
1. Verifique ID do Analytics:
   - Deve ser formato: G-XXXXXXXXXX
   - Verifique em index.html linhas 29 e 35

2. Aguarde dados:
   - Analytics pode levar 24-48h para mostrar dados
   - Use modo Real-Time para teste imediato

3. Teste com console:
   - Digite: window.getAnalyticsInfo()
   - Deve retornar: googleAnalytics: "Loaded"

4. Verifique bloqueadores:
   - AdBlock pode bloquear Analytics
   - Teste em modo anônimo sem extensões

5. Debug mode:
   - Adicione ao gtag config: { 'debug_mode': true }
   - Veja eventos no console
```

---

### Problema: Facebook Pixel não rastreia

**Sintomas:**
- Nenhum evento no Events Manager
- Pixel Helper mostra erro

**Soluções:**
```
1. Verifique Pixel ID:
   - Formato numérico: 123456789012345
   - Verifique em index.html linhas 41 e 51

2. Use Facebook Pixel Helper:
   - Extensão: Facebook Pixel Helper (Chrome)
   - Deve mostrar pixel ativo em verde

3. Teste eventos:
   - Click em link social
   - Console deve mostrar: fbq('track', 'Contact')

4. Verifique bloqueadores:
   - Extensões podem bloquear Facebook
   - Teste sem bloqueadores
```

---

### Problema: Site lento/travado

**Sintomas:**
- Animações com lag
- Scroll não suave
- Alto uso de CPU

**Soluções:**
```
1. Reduza partículas:
   - Edite js/particles.js
   - Linha ~16: Reduza getParticleCount()
   - Desktop: 80 → 40
   - Mobile: 30 → 15

2. Desabilite cursor customizado:
   - Comente linhas em js/cursor.js
   - Ou remova <script src="js/cursor.js">

3. Simplifique animações:
   - css/style.css → Comente @keyframes complexas
   - Remova efeitos parallax

4. Teste em outro dispositivo:
   - Pode ser limitação de hardware
```

---

### Problema: Layout quebrado no mobile

**Sintomas:**
- Elementos sobrepostos
- Texto cortado
- Scroll horizontal

**Soluções:**
```
1. Force viewport:
   - Verifique meta tag viewport no <head>
   - Deve ter: width=device-width, initial-scale=1.0

2. Teste responsividade:
   - F12 → Toggle device toolbar
   - Teste vários tamanhos

3. Verifique CSS:
   - Procure por larguras fixas (width: 1000px)
   - Use max-width ou percentuais

4. Media queries:
   - Verifique @media (max-width: 768px)
   - Ajuste estilos conforme necessário
```

---

### Problema: Cores não aparecem/Gradientes estranhos

**Sintomas:**
- Site todo preto e branco
- Gradientes não suaves
- Amarelo não aparece

**Soluções:**
```
1. Verifique variáveis CSS:
   - css/style.css linhas 13-17
   - Formato correto: #FFD700

2. Teste cores:
   - Inspecione elemento (F12)
   - Verifique computed styles

3. Suporte do navegador:
   - Gradientes podem não funcionar em navegadores antigos
   - Atualize navegador

4. Fallback colors:
   - Adicione cor sólida antes do gradiente:
   background: #FFD700;
   background: linear-gradient(...);
```

---

## 🔍 Ferramentas de Debug

### Console do Navegador
```
F12 → Console
- Veja erros em vermelho
- Warnings em amarelo
- Logs do sistema em azul
```

### Network Tab
```
F12 → Network
- Veja arquivos carregados
- Status 200 = OK
- Status 404 = Arquivo não encontrado
- Status 500 = Erro no servidor
```

### Elements Inspector
```
F12 → Elements
- Inspecione HTML em tempo real
- Veja CSS aplicado
- Modifique ao vivo para testar
```

### Device Toolbar
```
F12 → Toggle Device Toolbar (Ctrl+Shift+M)
- Teste em vários dispositivos
- iPhone, iPad, Android
- Custom sizes
```

### Lighthouse
```
F12 → Lighthouse
- Teste performance
- Acessibilidade
- SEO
- Best practices
```

---

## 📞 Ainda com Problemas?

Se ainda estiver com problemas:

1. **Verifique documentação completa**: README.md
2. **Revise código**: Comentários explicativos nos arquivos
3. **Teste exemplo funcionando**: Compare com original
4. **Copie mensagens de erro**: Console → Copy error message
5. **Teste em navegador diferente**: Chrome, Firefox, Safari

---

## ✅ Checklist de Verificação

Antes de buscar ajuda, confirme:

- [ ] Todos os arquivos estão no lugar correto
- [ ] Caminhos dos arquivos JS/CSS estão corretos
- [ ] JavaScript está habilitado no navegador
- [ ] Sem bloqueadores atrapalhando (AdBlock, etc)
- [ ] Navegador está atualizado
- [ ] Console não mostra erros críticos
- [ ] Testei em modo anônimo
- [ ] Limpei cache do navegador
- [ ] URLs dos links sociais estão corretas
- [ ] IDs do Analytics estão configurados (se usar)

---

**💡 Dica:** A maioria dos problemas é resolvida limpando o cache e testando em modo anônimo!
