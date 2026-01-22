# 🔗 Link na Bio - Landing Page Premium

![Status](https://img.shields.io/badge/status-active-success.svg)
![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

Landing page profissional estilo "link na bio" com design inspirado no Shopify Editions Winter 2026. Um site espetacular para centralizar todos os seus links de redes sociais em um só lugar.

## ✨ Características Principais

### 🎨 Design & Visual
- **Paleta de Cores**: Preto, amarelo, branco e cinza
- **Gradientes Animados**: Efeitos de gradiente sofisticados e dinâmicos
- **Design Responsivo**: Otimizado para todos os dispositivos (desktop, tablet, mobile)
- **Interface Moderna**: Estilo minimalista e profissional

### 🎭 Animações & Efeitos
- **Seção Hero Impactante**:
  - Sistema de partículas animadas no fundo (80+ partículas em desktop)
  - Texto com efeito de digitação (typing effect)
  - Animações de fade in e slide para títulos
  - Efeito glitch sutil no texto
  - Orbs de gradiente flutuantes com animação

- **Efeitos Parallax**:
  - Profundidade em múltiplas camadas
  - Movimento diferenciado baseado no scroll
  - Parallax nos elementos do hero
  - Efeito de repulsão das partículas com o mouse

- **Cursor Personalizado**:
  - Cursor customizado com efeito de seguimento suave
  - Mudança de cor baseada no elemento hover
  - Trail de partículas ao mover o mouse
  - Burst de partículas ao clicar
  - Efeito magnético em botões

- **Micro-interações**:
  - Efeito ripple nos cliques
  - Animações de hover nos cards de redes sociais
  - Efeito tilt 3D nos links
  - Glow effect nos botões
  - Rotação de ícones ao hover
  - Setas animadas

### 📊 Analytics & Rastreamento
Sistema completo de tracking implementado:

- **Google Analytics 4 (GA4)**:
  - Page view tracking
  - Click tracking em todos os links sociais
  - Scroll depth tracking (25%, 50%, 75%, 100%)
  - Time on page tracking
  - Conversion tracking
  - UTM parameters tracking
  - Heatmap data collection

- **Facebook Pixel**:
  - PageView automático
  - Event tracking para cliques
  - Lead tracking em CTAs
  - Contact events
  - Custom events personalizados

### 🌐 Redes Sociais Integradas
- Instagram
- YouTube
- TikTok
- Twitter/X
- LinkedIn
- GitHub
- Email
- WhatsApp

## 📁 Estrutura do Projeto

```
link-na-bio/
│
├── index.html              # Página principal
│
├── css/
│   └── style.css          # Estilos completos com animações
│
├── js/
│   ├── particles.js       # Sistema de partículas animadas
│   ├── animations.js      # Animações e efeitos parallax
│   ├── cursor.js          # Cursor personalizado e efeitos
│   └── tracking.js        # Google Analytics & Facebook Pixel
│
└── README.md              # Este arquivo
```

## 🚀 Como Usar

### 1. Personalização Básica

**Edite o arquivo `index.html`:**

```html
<!-- Altere seu nome -->
<span class="gradient-text typing-text">Seu Nome</span>

<!-- Altere sua descrição -->
<p class="hero-description">
    <span class="word">Criador</span>
    <span class="word">de</span>
    <span class="word">conteúdo</span>
    <!-- ... -->
</p>

<!-- Atualize suas estatísticas -->
<div class="stat-number">50K+</div>
<div class="stat-label">Seguidores</div>
```

### 2. Configurar Links de Redes Sociais

Substitua os links de exemplo pelos seus:

```html
<!-- Instagram -->
<a href="https://instagram.com/SEUUSUARIO" 
   class="social-link instagram-link" 
   data-social="Instagram">
   <!-- ... -->
</a>

<!-- YouTube -->
<a href="https://youtube.com/@SEUCANAL"
   class="social-link youtube-link"
   data-social="YouTube">
   <!-- ... -->
</a>
```

### 3. Configurar Analytics

**Google Analytics 4:**

No arquivo `index.html`, substitua `G-XXXXXXXXXX` pelo seu ID:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-XXXXXXXXXX'); // Seu ID aqui
</script>
```

**Facebook Pixel:**

Substitua `YOUR_PIXEL_ID` pelo seu ID do Facebook Pixel:

```html
<script>
    // ...
    fbq('init', 'YOUR_PIXEL_ID'); // Seu Pixel ID aqui
    // ...
</script>
```

### 4. Cores Personalizadas

Edite as variáveis CSS no arquivo `css/style.css`:

```css
:root {
    --color-yellow: #FFD700;        /* Amarelo principal */
    --color-yellow-light: #FFE55C;  /* Amarelo claro */
    --color-yellow-dark: #E6C200;   /* Amarelo escuro */
    /* Personalize conforme necessário */
}
```

## 🎯 Funcionalidades Detalhadas

### Sistema de Partículas
- 80 partículas em desktop, 30 em mobile
- Cores variadas: amarelo, amarelo claro e branco
- Efeito de repulsão ao mouse
- Conexão entre partículas próximas
- Pulsação sutil e glow effect

### Animações de Scroll
- **AOS (Animate On Scroll)**: Sistema personalizado
- Fade up, fade down effects
- Delays sequenciais para efeito cascata
- Threshold configurável
- Animações ativadas ao entrar no viewport

### Sistema de Cursor
- **Cursor principal**: Pequeno círculo dourado com glow
- **Follower**: Círculo maior que segue com delay
- **Trail effect**: Rastro de partículas ao mover
- **Click burst**: Explosão de partículas ao clicar
- **Magnetic effect**: Atração aos elementos interativos
- **Color change**: Muda cor baseado no elemento

### Tracking de Eventos

**Eventos Automáticos:**
- Page view (GA4 & FB Pixel)
- Scroll depth (25%, 50%, 75%, 100%)
- Time on page (10s, 30s, 60s, 120s, 300s)
- Page exit com tempo total

**Eventos de Interação:**
- Click em cada rede social (com identificação)
- Click em CTA buttons
- Email clicks
- WhatsApp clicks
- Conversão (engajamento do usuário)

**Dados Avançados:**
- UTM parameters tracking
- Heatmap data collection
- Click patterns
- Viewport information

## 📱 Responsividade

### Breakpoints
- **Desktop**: > 1024px (experiência completa)
- **Tablet**: 768px - 1024px (otimizado)
- **Mobile**: < 768px (simplificado)

### Ajustes Mobile
- Redução de partículas (30 vs 80)
- Desativação do cursor customizado
- Fontes responsivas com `clamp()`
- Padding e spacing otimizados
- Touch-friendly buttons

## ⚡ Otimizações de Performance

- **GPU Acceleration**: Uso de `transform: translateZ(0)`
- **Will-change**: Propriedades otimizadas para animação
- **RequestAnimationFrame**: Para animações suaves
- **Throttling**: Em eventos de scroll e mouse
- **Lazy Loading**: Preparado para imagens
- **Prefers-reduced-motion**: Respeita preferências de acessibilidade

## 🎨 Customização Avançada

### Adicionar Nova Rede Social

```html
<a href="https://sua-rede-social.com/usuario" 
   class="social-link novarede-link" 
   data-aos="fade-up" 
   data-aos-delay="500"
   data-social="NovaRede"
   target="_blank"
   rel="noopener noreferrer">
    <div class="link-background"></div>
    <div class="link-content">
        <div class="link-icon">
            <i class="fab fa-icone"></i>
        </div>
        <div class="link-info">
            <div class="link-title">Nova Rede</div>
            <div class="link-subtitle">Descrição</div>
        </div>
        <div class="link-arrow">
            <i class="fas fa-arrow-right"></i>
        </div>
    </div>
    <div class="link-glow"></div>
</a>
```

### Modificar Animações

No arquivo `css/style.css`, você pode ajustar:

```css
/* Velocidade das animações */
--transition-smooth: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
--transition-bounce: all 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);

/* Duração do float */
@keyframes float {
    /* ... ajuste aqui */
}
```

## 🐛 Debug & Monitoramento

### Verificar Status do Analytics

Abra o console do navegador e digite:

```javascript
window.getAnalyticsInfo()
```

Retornará:
```javascript
{
    googleAnalytics: "Loaded" / "Not Loaded",
    facebookPixel: "Loaded" / "Not Loaded",
    timestamp: "2026-01-21T...",
    page: "https://..."
}
```

### Console Logs

O sistema exibe logs detalhados:
- `📊 Analytics: Page view tracked`
- `📊 Analytics: Instagram link clicked`
- `📊 Analytics: Scrolled to 50%`
- `📊 Analytics: User spent 30 seconds on page`

## 🌟 Recursos Visuais

### Hero Section
- Badge animado "Disponível para conexões"
- Título com efeito glitch
- Nome com gradiente e typing effect
- Descrição com palavras animadas individualmente
- Estatísticas com contador animado
- Scroll indicator com animação

### Links Section
- Cards com background blur
- Hover effects sofisticados
- Cores específicas por rede social
- Arrows animadas
- Glow effect ao hover
- Ícones com rotação 360°

### CTA Section
- Card destacado com border animada
- Gradiente rotativo de fundo
- Botão com shadow animada
- Hover effect com scale

### Footer
- Logo animado
- Links sociais com hover effects
- Heart beat animation
- Waves animadas no fundo

## 📝 Meta Tags & SEO

O site inclui meta tags completas:
- Title e Description otimizados
- Open Graph (Facebook)
- Twitter Cards
- Favicon emoji
- Canonical URL ready

## 🔧 Tecnologias Utilizadas

- **HTML5**: Estrutura semântica
- **CSS3**: Animações e gradientes avançados
- **JavaScript (ES6+)**: Classes e módulos
- **Font Awesome 6**: Ícones vetoriais
- **Google Fonts**: Inter & Space Grotesk
- **Canvas API**: Sistema de partículas
- **Intersection Observer API**: Scroll animations
- **Google Analytics 4**: Web analytics
- **Facebook Pixel**: Event tracking

## 🎓 Conceitos Implementados

- **Object-Oriented Programming**: Classes para cada sistema
- **Event-Driven Architecture**: Listeners e handlers
- **Responsive Design**: Mobile-first approach
- **Progressive Enhancement**: Funciona sem JavaScript
- **Accessibility**: Semantic HTML, ARIA labels
- **Performance**: Otimizações e best practices

## 📦 Deployment

### Opção 1: GitHub Pages
1. Crie um repositório no GitHub
2. Faça upload dos arquivos
3. Ative GitHub Pages nas configurações
4. Acesse via `username.github.io/repo-name`

### Opção 2: Netlify/Vercel
1. Conecte seu repositório
2. Deploy automático
3. Custom domain disponível

### Opção 3: Hospedagem Tradicional
1. Faça upload via FTP
2. Aponte domínio
3. Configure SSL

## 🔒 Segurança

- Links externos com `rel="noopener noreferrer"`
- Sem exposição de dados sensíveis
- Scripts de terceiros apenas de fontes confiáveis
- Content Security Policy ready

## 📄 Licença

Este projeto está sob a licença MIT. Você é livre para usar, modificar e distribuir.

## 🤝 Contribuições

Melhorias são bem-vindas! Sinta-se à vontade para:
- Reportar bugs
- Sugerir novas features
- Melhorar documentação
- Otimizar código

## 📧 Suporte

Para dúvidas ou suporte:
- Verifique a documentação completa
- Consulte os comentários no código
- Use o console para debug

## 🎉 Agradecimentos

Design inspirado no incrível trabalho do Shopify Editions Winter 2026.

---

**Feito com ❤️ e muito ☕**

*Última atualização: Janeiro 2026*
